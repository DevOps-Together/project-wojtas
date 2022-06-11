# Blokwoanie stackoverflow
Stackoverflow korzysta z AWSowego Route53 jako DNS-a. Można podejrzewać, że DNS kieruje na usługi w AWS, a co za tym idzie adresacja może być dynamiczna.
1. Blokada IP
    * Na routerze blokujemy z puli adresów dynamicznych aktualnie zwracane adresy stackoverflow. Opcjonalnie można na podstawie adresu MAC przyjdzielić w DHCP konkretny adres IP, wtedy reguły mogą być lepiej targetowane. 
    * słabość - adres stackoverflow może się zmienić
    * słabość - Student może ominąć blokadę ustawiając sobie inny adres IP z zakresu podsieci, ale z poza blokowanych adresów
1. Ulepszona blokada IP
    * Piszemy skrypt, który sprawdza aktualne wpisy w DNS stackoverflow.com i blokuje, dla zakresu adresów dynamicznej puli adresowej, aktualne adresy stackoverflow za pomocą iptables. Skrypt odpalamy cyklicznie z crona. Skrypt powinien również usuwać stare wpisy. 
    * słabość - Student może ominąć blokadę ustawiając sobie inny adres IP z zakresu podsieci, ale z poza blokowanych adresów.
1. Ulepszona blokada IP v2
    * Piszemy skrypt, który sprawdza aktualne wpisy w DNS stackoverflow.com i blokuje, dla całej podsieci, aktualne adresy stackoverflow za pomocą iptables. Dla naszej stacji ze stałym IP dodajemy reguły przepuszczające ruch (mogą przepuszczać cały :->). Skrypt odpalamy cyklicznie z crona. Skrypt powinien również usuwać stare wpisy. 
1. Podmiana w DNS (a'la ustawa antyhazardowa)
    * Na routerze instalujemy dnsmasq i w /etc/hosts dodajemy wpis, który rozwiązuje stackoverflow.com na adres innej strony. Na przykład na kontrolowany przez nas serwer, który na vhoście dla domeny stackoverflow.com zwróci błąd http 500 lub 404. 
    * słabośc tego wariantu polega na tym, że Student może zmienić DNS na inny.
1. Proxy
    1. Stawiamy proxy http (np: squida) na routerze
    1. Blokujemy wyjście do internetu dla całej podsieci, oprócz naszego komputera (ze statycznym IP). Wypuszcamy tylko wybrane protkoły.
    1. Ustawiamy DHCP aby zwracało proxy (https://serverfault.com/questions/707586/is-it-possible-to-configure-proxy-setting-through-dhcp)
    1. Blokujemy dostęp do stackoverflow.com w squidzie
    * Dodatkowy sukces - podnosimy bezpieczeństwo odcinając komunikację poza wybranymi protokołami.
