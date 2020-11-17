## Bot dla firmy medycznej

### Use case

Bot jest pomocą dla serwisu technicznego firmy medycznej (tutaj Roc Med). Firma medyczna produkuje sprzęt medyczny i odczynniki. Posiada swoje call center. Bot jest pierwszą linią pomocy dla klientów. Ma pomóc w odciążeniu pracowników od udzielania często zadawanych pytań. Bot również zbiera różne informacje i dane, które później mogą posłużyć pracownikom do wykonania kolejnego zadania. 

Zadania bota:

* Udzielanie odpowiedzi na pytania typu jak złożyć reklamację. --> Zapytanie użytkownika czy ma formularz reklamacji --> Jeśli użytkownik odpowie, że tak, to bot odpowiada, że według podanych wcześniej wskazówek powinien uzupełnić i wysłać formularz -- Jeśli użytkownik odpowie, że nie, to bot prosi o podanie adresu e-mail, który zapisuje i informuje użytkownika, że na ten adres e-mail zostanie wysłany odpowiedni formularz.
* Udzielenie odpowiedzi na pytania dotyczące statusu reklamacji. --> Bot zbiera od użytkownika informacje: numer klienta, datę złożenia reklamacji, adres e-mail i informuje, że na wskazany adres mejlowy zostaną przesłane informacje odnośnie tej reklamacji.
* Gdy użytkownik napisze informację, że jakiś aparat medyczny się zepsuł, bot zbiera dane: numer klienta, numer seryjny aparatu, numer telefonu i informuje, że inżynier niezwłocznie oddzwoni do klienta, również prosi o krótki opis awarii.
* Udzielenie informacji o wykonywaniu przeglądów . --> Bot informuje, że firma stara się wykonywać przeglądy na czas i zazwyczaj dwa dni przed końcem przęglądu pracownik dzwoni do kleinta umówić się na spotkanie. Bot pyta czy uzytkownik, chce ustalić konkretną datę przeglądu. --> Jeżeli użytkownik odpowie, że tak, to bot prosi o podanie numeru klienta, numeru seryjnego aparatu oraz preferowaną datę przeglądu. Bot informuje, że w odpowiednim czasie, pracownik skontaktuje się (pracownicy dzwonią do klientów według swoich list, więc bot nie musi prosić o podanie numeru telefonu) z klientem i spróbuje dostosować się do preferencji klienta. -- Jeżeli użtkownik odpowiedział, że nie chce ustalać daty przeglądu bot informuje, żeby oczekiwać telefonu.
* Instruowanie klienta co zrobić, gdy ten zgłasza zepsuty sprzęt peryferyjny (monitor, UPS itp. dołączany do aparatów medycznych). Bot odpowiada, że firma wyśle niezwłocznie nowy sprzęt. Prosi klienta o podanie modelu sprzętu, jego numeru seryjnego oraz numeru seryjnego aparatu, do którego był dołączony oraz numeru kleinta. Bot również prosi o podanie adresu i prosi o spakowanie starego sprzętu w opakowanie od nowego i powiadomienie firmy o tym, aby firma mogła odebrać ten stary sprzęt do utylizacji.
* Zbieranie informacji od klienta, gdy ten zgłasza, że można odebrać stary sprzęt peryferyjny. Klient podaje: numer seryjny sprzętu, swój numer klienta oraz adres.
* Kiedy użytkownik napisze 'help' albo poda jakieś inne hasło nie związane z powyższymi scenariuszami, bot wyświetla informacje, na jakie kategorie pytań udziela odpowiedzi.

### Kroki budowania bota

Korzystałam z serwisu LUIS i Bot Framework Composer.

#### LUIS

##### Utworzenie zasobu usług:

1. Utworzenie zasobu LUIS w Azure portal "Create a resource".
2. Nazwanie zasobu LUISMEDY.
3. Wybranie odpowiedniej subskrybcji (Azure dla studentów).
4. Utworzenie nowej grupy zasobów LearnRG.
5. Wybranie lokalizacji nabliższej mojej - west europe.
6. Wybranie darmowej opcji LUISa. 
7. Zachowanie kluczy. Klucz 1 był później potrzebny w Bot Framework Composer.

Na poniższym obrazie znajduje się okno LUISMEDY z kluczami.
<img src="Images/luis1.png" width = 800> 

##### Utworzenie aplikacji LUIS:

Utworzenie aplikacji w tym samym geograficznym regionie, co serwis. 
1. Zalogowanie się do LUIS https://eu.luis.ai/ jak do konta Microsoft.
2. Utworzenie aplikacji z nazwą LUISMED.
3. Utowrzenie odpowiednich zamiarów i podmiotów. Do zamiarów zależy podaj przykłady wejściowe. Podmiotami oznacza się odpowiednie wyrazy w przykładowych zdaniach z intencji.

Na poniższym obrazie znajduje się okno ze stworzonymi zamiarami.
<img src="Images/luis2.png" width = 800> 

Na poniższym obrazie znajduje się okno ze stworzonymi podmiotami.
<img src="Images/luis3.png" width = 800> 

4. Wytrenowanie i testowanie modelu LUIS.
5. Upublicznienie aplikacji.


#### Bot Framework Composer

##### Instalacja
Procedura instalacji Bot Framework Composer na Windowsie:
1. Przygotować środowisko - zainstalować .NET Core SDK 3.1 lub najnowszą wersję, pobrać z: https://dotnet.microsoft.com/download/dotnet-core/3.1.
2. Przygotowanie środowiska - zainstalować Bot Framework Emulator, pobrać z: https://github.com/microsoft/BotFramework-Emulator/releases/latest.
3. Zainstalować Bot Framework Composer, pobrać z: https://aka.ms/bf-composer-download-win.


##### Kroki budowy bota w Bot Framework Composer
1. Utworzenie nowego bota o nazwie RocMed.
2. Dodanie dialogu powitalnego użytkownika, który wyświetla się na początku dialogu z botem.
Na poniższym rysunku przedstawiony jest dialog powitalny. 
<img src="Images/luis4.png" width = 800> 
3. Utworzenie wyzwalaczy do obsługi sześciu zadań i 'help'.
Na poniższym rysunku pokazany jest wyzwalacz przekierowujący do dialogu dotyczącego pytania jak złożyć reklamację. Z prawej strony wpisane są frazy wyzwalacza. Wyzwalacze dodane są z LUISa. W panelu nawigacyjnym RocMed we właściwościach należało jako rozpoznawalny typ ustawić LUIS.
<img src="Images/luis5.png" width = 800> 
4. Utworzenie dialogów, które są rozpoznawane przez konretne wyzwalacze.
Na poniższym rysunku znajduje się fragment dialogu. Po prawej stronie widać, że bot zapisuje zmienną podawaną przez użytkownika w pamięci - user.confirmed.
<img src="Images/luis6.png" width = 800> 
Na poniższym rysunku znajduje się jeden z dialogów, w którym wykorzystany został bloczek if/else.
<img src="Images/luis7.png" width = 800> 
5. Po naciśnięciu Start Bot (pierwsze uruchomienie bota), a później Restart Bot pojawiało sie okno, w którym należało wpisać klucz główny wygenerowany przez LUIS. W taki sposób bot połączył się z utworzonym wcześniej zasobem LUIS.
6. Testowanie dialogów
Na poniższym rysunku znajduje się przykładowa rozmowa użtkownika z botem.
<img src="Images/luis8.png"> 

* architektura
* kod + dane niezbędne do reprodukcji        

### Nagranie

https://youtu.be/ZeJjKcqm0G8

Nagranie jest to DEMO mojego bota, które obrazuje środowisko Bot Framework Composer i przykładowy dialog zadziałania. W tym, krótkim filmie zostały wymienione najważniejsze elementy bota. Pokazałam scenariusz rozwiązania problemu przez bota. Klient zapytał jak złożyć reklamację i poprosił o odebranie starego UPSa. 


### Podsumowanie

Uważam, że tworzenie bota to niezwykle satysfakconujące zadanie. Bot zrobiony przeze mnie spełnia moje założenia - umie wykryć jakie zapytanie pasuje do odpowiedniego dialogu i zadaje konkretne pytania. Uzyskałam to dzieki zastosowaniu LUIS.
Oczywiście ten bot może, a nwet powinien być dalej rozwijany, można mu dodać wiele funkcji.
Jedną z taki możliwości, jest dodanie opcji wysyłania mejla do pracownika (na wskazany, ustalony adres e-mail) z danymi uzyskanymi od użtkownika w trakcie rozmowy. Tutaj: https://microsoft.github.io/botframework-solutions/skills/samples/email/ jest opisana funkcja poczty. Myślę, że możnaby skorzystać z tego luz zaproponować jakieś inne rozwiązanie do wysyłania mejli przez bota. 
