**Mój pierwszy raz**

Twój ~~pierwszy~~ zerowy dzień w firmie. Przychodzisz i widzisz, że masz standardowego PECeta (jakiś gruz gorzej niż z bazaru) a nie laptopa ;(
Po chwili kręcenia się przy swoim nowym biurku idziesz na rozmowę do szefa. Po 3 słowach poznajesz, że jest to Janusz i od dziś zaczynasz pracę w JANUSZEX Z O.O.
Spoko jest to, że polaczek biedaczek oszczędza na wszystkim, więc w biurze będzie tylko sam Linux i to Ubuntu - to chyba jedyna pozytywna rzecz w tej firmie xD

 - przygotuj swoje stanowisko do pracy

Godzina 16 - czas do domu a Ty nie zrobiłeś nic konkretnego - standard.

**Następny dzień**

Przychodząc rano do biura - do razu jesteś proszony do Janusza na dywanik.
Szef byl wczoraj na siłowni i jego koledzy (też prezesi) flexowali się swoimi stronami firm.
Janusz cały sie zagotował, że on nie ma czegoś takiego – myślisz sobie, „oho zaczynają się kłopoty”. Trzeba będzie pewnie postawić Wordpressa. 

Mówisz szefowi o zapotrzebowaniu na serwer, odpowiedź jest prosta nie ma to kasy (ale pakiet nowych odżywek stoi obok biurka). 
Musisz coś wykombinować. Wpadasz na pomysł, że zrobisz to na swoim kompie pod biurkiem:
  1. Zainstaluj Virtualbox;
  2. System operacyjny jaki chcesz - preferowany Ubuntu Server;
  3. Połącz się z nim przez puppy ( zainstaluj ssh);
  4. “Postaw” wordpressa - najchętniej apache -  zobacz co jest w pliku wp config.php i .htaccess (nie będę pisał jak to zrobić jest całe mnóstwo gotowych tutoriali – jeżeli  masz problem #MAM PROBLEM POZIOM 0 - https://discord.com/channels/786670250301063189/978961864736268318);
  5. Przekieruj port 80 tak aby był widoczny z IP twojego kompa - sprawdź czy dziala to w twojej lokalnej sieci;
  6. Dodaj jakis obrazek do WP - tak zeby nie był az taki pusty - zakładka media w panelu admina;
  7. Wyślij login i hasło do swojego szefa do panelu admina WP i URL (tak na niby..);
  8. Koniec dnia.

**Następny dzień**

Szefa jeszcze nie ma - bawisz sie ustawieniami VB - zmień by Virtualbox nie pracował w trybie sieciowym NAT a bridge (mostka).

![VB](img/VB1.jpg?raw=true "VB network")

 
  - Uruchom ponownie maszynę i sprawdź jaki ma IP i jak możesz teraz sie z nią połączyć.
    Dlaczego tak się stało?
    (Dodatkowo) Opisz w kilku słowach w GIT przez strone www (https://github.com/DevOps-Together/project-wojtas/tree/main/level/0/comments) dodaj plik w folderze poziom zero ze swoim nick i napisz co sie stało. 

W południe przychodzi szef - jest bardzo wku**** - próbował pokazać stronę kolegom pod adresem URL, który mu wczoraj wysłałeś. 
 <span style="color:red">Wyskoczyło coś tam connection i nie pokazywało się nic</span>. **Masz to jak najszybciej naprawić**. 

Mowisz cos o domenach i o tym, że końcówką .pl kosztuje około 100 netto. Szef schodzi prawie na zawał. Mówi, że za 100 ziko to kupić może cały zestaw śliwczanu kreatyny.

Odsyła cię z kwitkiem – musisz coś wymyśleć.
Wracając po drodze dowiadujesz, że urządzeniem brzegowym w firmie jest jakiś 20 letni (o zgrozo) TP-link .

<details><summary>Opcjonalnie - jeśli chcesz i możesz</summary>
Wystaw swoją stronę WP na świat w swoim domowym labie.
Oczywiste jest to, że trzeba zrobić port forwarding na routerze - jeśli tego nie wiesz napisz o tym na #MAM PROBLEM POZIOM 0. Mozesz też dodać darmowa domenę https://freedns.afraid.org/ lub https://freedns.42.pl/.
</p>
</details>

Przychodzi żona szefa - Grażyna :D - próbowała wypełnić treściami WP ale mówi, że dane które jej wysłałeś do logowania nie działają.

  - Zaloguj się do MySQL i zmieć hasło dla admina - tak przez konsole (polecenie update);

W Wordpressa i pehape coraz lepiej ci idzie, gdzies na forum wyczytałeś ze warto zabezpieczyć panel admina /admin auth_basic tak by internetowe boty nie skanowały podatności.
  - Zrób to!  Dodaj dwóch userów Janusz i Grażyna;

Dowiadujesz się że jutro przychodzi dEvElOpEr Wordpress.

**Następny dzień**

Od rana spotykasz nowego kolegę - jakiś student, który jeszcze się uczy i pracuje na śmieciówce (bo jakże inaczej). Sytuacja jest identyczna jak u Ciebie - od rana idzie do szefa na rozmowę. Wracając prosi Cię o środowisko testowe dla swojego WP.

  - **Easy way** - klon w VB albo **hard way** (recommend) - Zainstaluj nowy system ubuntu zrób kopie plików WP przy pomocy SCP lub/i rsync (możesz porownać czas). Zrób dump bazy danych (kopiowanie) i restore lub/i przez pipe (porównując czas).

Nowy kolega mówi że IP serwera ok jest dobre ale przekierowuje go ciągle na ten poprzedni.
  - Poszukaj odpowiedzi w bazie danych - jesli bedziesz mial problem wiesz gdzie pisać.
  - Aaa i wspominal cos o SFTP jak moze sie polaczyc by wrzucać pliki przez Filezilla 
      - https://devanswers.co/configure-sftp-web-server-document-root/

Kończąc swoją pracę zauważasz, że nie ma Internetu w biurze. Po szybkiej diagnozie wygląda ze TP-link w dniu dziś odmówił dalszej współpracy ;( Rest In Pepperonis 

KONIEC poziom 0 - jeżeli zrobiłes przekierowanie portów na swoim domowym routerze to odwróć zmianę.

Podziekowania dla @https://github.com/bishtou
@bishtou
