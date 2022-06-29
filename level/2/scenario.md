Kota nie ma to myszy harcują, a jak nie ma szefa to informatycy hakują :D 


>>**Dzień 1**

Wracasz po weeknedzie...

Ale jak to? Nie ma szefa? Pytasz koleżnaki(rekruterki) - TAK, nie go przez całe 2 tygodnie. Wybrał się na yacht na Malediwy. 
Wychodząc z pokoju HR, miałeś już na końcu języka: "hip hip hura!" - ale miła koleżanka z działu HR dodała, że szef zostawił Ci firmową kartę - tak na wypadek nieprzewidzianych zakupów.
No to takie wiesci, że nic tylko "zesrać się" ze szczęścia :D

Radość jednak nie trwa zbyt długo, bo kiedy poszedłeś za "potrzebą", na twój prywatny telefon dzowni już boss - Janusz.
Jest koniec miesiąca a on musi pobrać raport dla ksiegowej. Pojawia się jednak problem - on jest TAM a dane TU - w firmie.
Mowisz mu o VPN - ale jego to nie intersuje: "ma działać i kup co trzeba - przecież masz firmową kartę" mowi, rozłączając się.

Twoja pierwsza myśl to wymarzone, od dawna wyczekiwane, wyśnione przez te wszytkie dni - REMOTE WORK!!!
Już nie będziesz musiał siedzieć z tym debilem w jednym pokoju ale w swoim domku, no i do tego ta karta...
Chyba podbijanie świata przez nadpisanie DNS'ów wzbudziło respekt u szefa. 

Odrazu guglujesz najtańszego VPSa dostepnego na rynku. W porównaniach najlepiej wypada Hetzner. 
Dokonujesz zakupu - wpisujesz numer karty, CVV, jeszcze znak krzyża by się udało. Jest - masz pierwszego własnego VPSa
(my nie mamy - @TORGiren nam zasponsorował - kudos) !

Ale na dzis fajrant - dochodzi 16 :)


>>**Dzień 2**

Od rana, jeszcze w biurze, cieszysz się swoim VPSem - ale robota czeka.

**Zadanie**

Na początek "przeklikując" postaw VMke na Proxmox'ie (nie będe opisywał jak - na YT jest masa tutoriali). 
Poproś w wątku - https://discord.com/channels/786670250301063189/991589776954245120, o dostęp do serwera PROXMOX.

A jesli masz problem to pomocy szukaj
https://discord.com/channels/786670250301063189/991589619474903110

UWAGA!!! 
Mamy mało miejsca na dysku i wolnych portow, więc razem z wstawieniem servera VPN otrzymasz port, na którym mozesz wystawić uslugę. 
Po skończeniu zadania usuń VMke, żeby zwolnić innym zasoby potrzebne do wykonania zadania. 

Na tej wirtualnej maszynie zainstaluj server VPN.
Wygeneruj klucze dla siebie i dla Janusza. Sprawdz czy tunel zestawia się poprawnie. 

Wracasz do do domu.
Po godzinach stwierszasz ze obejrzałbyś jakąś nowość kinową, ktora jest dostepna tylko w USA.

**Zadanie**

Zrób tak, żebyś TYLKO TY miał dostep do jednej strony (np. http://ifconfig.co) przez VPNa.


>>**Dzień 3 - znów w biurze**

Przez oglądanie seriali po nocy, nie jesteś wyspany; obudził Cię telefon-"zjeba" od Janusza - nie ma dostepu do firmowych danych.

**Zadanie**

Na nowej VM w twojej grupie (VirtualBox), pod nazwą "openvpn-client" postaw klienta OpenVPN. Skonfiguruj wszystko tak, by tunel się zestawił.
Dlaczego to rozwiązanie jest złe? Jakie ma wady? Zobacz czy masz dostęp do Wordpress'a po wewnetrznym adresie IP. Jakie IP widzi serwer apache? Przyjrzyj się wpisom w logach.
Przenieś klienta VPNa na router - jaka jest różnica (trochę bez sensu łączyć się przez serwer w USA do własnego Virtubalboxa - ale czego się nie robi w imie nauki)?


>>**Dzień 4 i 5**

Kolega z innej firmy polecił, by zautomyatyzowac caly proces wdrażania.

**Zadanie** 

Przez to będziemy często usuwać VMki, napisz automatyzację do jej tworzenia.
Kod terraform + playbook z ansible'a wrzuć do repozytorium, do folderu ze swoim użytkownikiem - PAMIĘTAJ BY NIE DODAĆ LOGINU I HASŁA DO REPOZYTORIUM !!!
Zrób jak najwięcej używając komend git'a, a nie przez stronę WWW.

Podziekowania dla @wwakas aka mv5112 https://discordapp.com/users/419915779216244737
i jak przy poprzednich levelach @bishtou https://discordapp.com/users/146392684536397824
