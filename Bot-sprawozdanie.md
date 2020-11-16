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
#### LUIS

<img src="Images/UserInput.PNG" width = 600> 


#### Bot Framework Composer
* kroki budowania
* architektura
* kod + dane niezbędne do reprodukcji
1. instalacja bot framework composer
początek powitanie.
2. Add new dialog
HowtoMakeComplaint 
        
* Video na YouTube (public/unlisted) z demo / pitch demo waszego bota (około 3 do 5 minut) i Waszym komentarzem:
* Jaki problem rozwiązuje Was bot (scenariusz)
* Na czym polega rozwiązanie i jak działa


### Nagranie

https://youtu.be/ZeJjKcqm0G8

Nagranie jest to DEMO mojego bota, które obrazuje środowisko Bot Framework Composer i przykładowy dialog zadziałania. W tym, krótkim filmie zostały wymienione najważniejsze elementy bota. Pokazałam scenariusz rozwiązania problemu przez bota. Klient zapytał jak złożyć reklamację i poprosił o odebranie starego UPSa. 


### Podsumowanie
