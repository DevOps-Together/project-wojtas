**No i jesteśmy** 


To znaczy Ty i cała firma -  w średniowieczu. 
Słuchasz radia, takiego normalnego FM, czytasz gazekę z Lidla - no bo w pracy, Janusz, zabrania mieć prywatny telefon ;/. Z pokoju szefa słychac tylko same przekleństwa i muzyczkę oczekiwania na lini, bo szef dzwoni do ISPa. “Jak by to była ich wina” - śmiejesz sie w głowie sam do siebie :D. Po prawie godzinie oczekiwania, wychodzi szef - cały czerwony - jak by wrócił z wakacji z Chorwacji i pyta się czy masz jakiś pomysł.

Nie pracujesz tu od wczoraj więc odpowiedź jest prosta - 
TO JA ZROBIĘ SAM ROUTER!!!
Szef jest w takim szoku ze zmienił kolory.

Tłumaczysz mu że bedzie potrzebny do tego komp i ze możesz poświęcić swój, ale w zamian chcesz coś innego. 
Grażyna natychmiast przytakuje ze można zabrać kompa Dzesiki, a dla niej z zamian kupic nowy (bo za chwile ma urodziny czy inny dzien dziecka).
W kanciapie znajdujesz sieciowkę na PCI-e o której już dawno ktoś zapomiał.
Robisz reinstall swojego kompa i cala sieć wyglada teraz tak:

![boom](img/siec.png?raw=true "siec")

W tym czasie szef przywozi komputer Dzesiki. Jest caly zawalony jakimiś najróżniejszmy naklejkami. Stickerbomb to przy tym nic. 

To jest stickerbomb :D

![boom](img/sticketbomb.jpg?raw=true "stickerbomb")

Całe szczęście że ma i5, 16G RAMu oraz dysk SSD - jest już na czym pracować :)

**Zadanie**. 
- Utwórz nową VM i dodaj do niej drugi interfejs sieciowy (internal network)

![VB](img/VB2.png?raw=true "VB network")

Pozostałe dwa systemy przestaw by też korzystały wyłacznie z tej sieci wewnętrznej. 

Od tej chwili będziemy tę maszyne nazywać ROUTER albo GATEWAY. Więc warto by przestawić nazwe w VB i hostname na którąś z tych.

Na ROUTER zrób tak żeby teraz Linux byl własnie routerem (bez DHCP i DNS - jeszcze).
Warto wyznaczyc adresację, której potem musisz sie trzymać!
Na jednej VMce dodaj statyczny adres - zobacz czy działa ping do jakiejś domeny.
Pobaw sie tcpdump na gateway np.

`tcpdump -iany` 

Zobacz jak wygladą ruch, czy widzisz te same pakiety dwa razy? 
Dla potrzebujących - napisz na #mam problem (https://discord.com/channels/786670250301063189/982994686098702349) jak nie wiesz jak, ale zanim to zrobisz pomyśl co jest potrzebne by komptuery mogły ze sobą rozmawiać :D 

Ok - no to już masz swojego kompa, nowy system, od razu widac ze dysk SSD robi robotę. 
Aż chce się pracować, a roboty jest dużo bo narazie tylko ty masz dostep do Internetu. Spryciula dodałeś sobie statycznie adress IP z puli. Żeby jeszcze bardziej zdenerować swojego (nie)kolege studenta, puszczasz muzyke z YT (:D) i czekasz na reklamy. “Wypróbuj subskrybcji premium na YOUTUBE”!!! 


Na router doinstaluj DHCP lub dnsmasq. Zrób tak żeby druga VMka pobrała addres.
Jako DNS wybierz 1.1.1.1 lub 8.8.8.8.

Potwierdź, że Internet z VMki działa.

**Następny dzień**

Jestes zachwalany przez szefa i koleżnaki z pracy. Na Twoim biurku jest małe ciasto.
Twój kolega WP developer jest nie w sosie od rana. Pytasz co sie stało.
W odpowiedzi uzyskujesz że nie może nic wgrać na SFTP.
Masz dobry humor to pomożesz temu nieszczęsnemu biedakowi. Logujesz sie przez ssh na testowy WP i...

“”Wykonaj polecenie 
!!! UWAGA !!! nie rób tego na swoim PC - ma byc to zrobione w VMce w VB
`fallocate -l 50G big_file`
“”

Sprawdzasz zajetość dysku, a tam 100% 

Rozszerz dysk na tej VMce.

**Następny dzień**

Grażyna wpada do pokoju, drze się i miota jakby by ją opętał jakiś szatan.
Z słów które wypływaja z jej ust rozumiesz że kolega developer na wszystkich artykułach wpisał JANUSZ-SEX. Beka ma maksa, aż się popłakałes ze śmiechu.
Ale poprawiać po nim będziesz musiał TY.

Google zaindekstowalo już stronę /JANUSZ-SEX 

Zrób rewite żeby nazwa strony była ok.

Zostaje kwestia tekstu który jest w WP.
Poszukaj w necie czy da sie co z tym zrobić i to bez update MySQL
<details><summary>Hint</summary>
https://httpd.apache.org/docs/2.4/mod/mod_substitute.html
</p>
</details>

**Następny dzień**

Twój współpracownik wkurwił Cię. 
Ma już na koncie 3 minusy: 
   - Zjadł kawałek Twojego ciasta;
   - Nie chciał pożyczyć Ci 2 złote na Twojego ulubionego enegetyka;
   - Zamiast napisać JANUSZEX napisal JANUSZ-SEX i do tego ten dysk (to Twój cenny dysk SSD)
   
Więc jak to mówi stare chińskie przysłowie:

![VB](img/przyslowie.jpeg?raw=true "przyslowie")

Przez ramie widziałeś, że (nie) kolega kopiuje cały kod z Stackoverflow.

**Zadanie**

Udajac, że Twoja testowa WP VMka - ta z dynamicznym IP - to komp studenta, zablokuj mu dostęp do Stackoverflow.
Sprawdź w Links czy blokada działa poprawie.
Sposobów jest kilka - opisz je w GIT.


**Ostani dzień tygodnia - prawie weekend**

Szef chodzi po pokoju jakby jego Iwatch kazał mu zrobić 10 kilometrów - ale to nie był on (w sensie zegerek) tylko jego nowe kokosowe dopalacze (pewnie rozkruszone batony Kizzersa).

Janusz podchodzi do Ciebie bardzo blisko, wasze nosy prawie sie spotykają.
Mówi że od teraz przejmujemy cały Internet.
Masz zrobić tak zeby wpisujac google.com i google.pl pokazywał się tekst:

**“JANUSZ RONDZI SWIATEM”**

Ooo żesz kur*** gdzie ja pracuje...

CDN
Jak przy level 0 - podziekowania dla @https://github.com/bishtou @bishtou





