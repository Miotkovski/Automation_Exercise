# Przypadki testowe: Automation Exercise

## 1. Moduł: Rejestracja i Zarządzanie Kontem

> ** Notatka techniczna: ** > Przypadki testowe w module Rejestracji zostały zaprojektowane jako **scenariusz zależny**. <br>
> Zestaw 'DATA-01' jest celowo współdzielony między TC-01 a TC-02

## 🪪 Dane Testowe (Test data Pool)
| ID Danych | Imię / Nazwisko | E-mail | Hasło | Szczegóły (Płeć, Data ur. Adres, nr telefonu) | Company | Checkboxy | 
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **DATA-01** | Jan QA | tester_jan@poczta.pl | Pasword123 | Pan, **12/05/1990**, <br>USA, California, Los Angeles, <br>Sezamkowa 10, 90001, <br>nr.tel: 123456789 | Test Company | Newsletter: TAK, Offers: TAK |

| ID Danych | Przeznaczenie | Imię na karcie | Numer karty | CVC / Expiry | 
| :--- | :--- | :--- | :--- | :--- |
| **DATA-02** | Płatnośc testowa | Jan | 4111111111111111 | CVC: 123, Exp:01/2030 |




| ID | Tytuł | Warunki testowe | Kroki testowe | Oczekiwany rezultat |
| :--- | :--- | :--- | :---| :--- |
| **TC-01** | Skuteczna rejestracja nowego użytkownika | Użytkownik nie posiada konta na platformie | 1. Wejdź na stronę główną.[Automation Exercise](https://automationexercise.com) <br>2. Kliknij przycisk 'Sign Up' / Login<br>3. W sekcji 'New User Signup!' wprowadź dane(**DATA-01**).<br>4. Kliknij 'Signup'.<br>5. Wypełnij formularz (**DATA-01).<br>6. Kliknij 'Create Account'. | Wyświetla się komunikat: 'ACCOUNT CREATED!' oraz przycisk 'Continue'.|
| **TC-02** | Próba rejestracji na istniejący e-mail | Istnieje jużkonto zarejestrowane na e-mail: 'jan_tester@poczta.pl_' | 1. Wejdź na stronę 'Signup / Login'<br>2. Wpisz nazwę i e-mail: **DATA-01**.<br>3. Kliknij 'Signup'. | Pojawia się komunikat o błędzie: 'Email Address already exist'. |
| **TC-03** | Usunięcie konta użytkownika | Użytkownik jest zalogowany na swoje konto. | 1.Kliknij przycisk 'Delete Account.<br> 2. Konto zostaje usunięte. | Wyświetla się komunikat 'ACCOUNT DELETED!'. |
| **TC-04** | Dodanie produktu do koszyka jako Gość | 1.Użytkownik nie jest zalogowany.<br>2.Koszyk jest pusty. | 1.Wejdź na stronę główną [Automation Exercise](https://automationexercise.com)<br>2.Przewiń w dół do sekcji **'Features Items'**.<br>3.Najedź myszką na pierwszy dostępny produkt (np.'Blue Top') i kliknij **'Add to cart'**.<br>4.W oknie modalnym (pop-up), które się pojawi, kliknij przycisk **'View Cart'** | 1.Użytkownik zostaje przekierowany do widoku koszyka ('/view__cart')<br>2.Produkt 'Blue Top' jest widoczny na liście.<br>3.Ilość (Quantity) wynosi 1, a cena zgadza się z ceną na stronie głównej(500).<br>4.Użytkownik nie został poproszony o logowanie na tym etapie. |
| **TC-05** | Próba przejścia do płatności (Checkout) jako Gość |1. Użytkownik nie jest zalogowany.<br>2.W koszyku znajduje się conajmniej jeden produkt.| 1.Przejdź do widoku koszyka ('/view_cart').<br>2.Kliknij przycisk **'Proceed To Checkout'**. | 1.Pojawia się okno modalne (pop-up) z komunikatem: 'Checkout: Register / Login to proceed checkout'.<br>2.Użytkownik widzi dwie opcje 'Register/Login' oraz 'Continue On Cart'.<br>3.System **nie pozwala** na przejście do strony z danymi wysyłki bez założenia konta(strona '/checkout') nie powinna się załadować. |
| **TC-06** | Próba przejścia do checkout po logowaniu | Użytkownik jest w widoku ('/view_cart') jako Gość.<br>W koszyku znajduje się produkt. | 1.Kliknij przycisk **'Proceed To Checkout'**.<br>2.W oknie modalnym (pop-up) kliknij link **'Register / Login'**.<br>3.Zaloguj się używając **DATA-01**.<br>4.Po ukończeniu logowania i kliknięciu 'Continue', wróć do koszyka i ponownie kliknij **'Proceed To Checkout'**. | 1.System pomyślnie loguje użytkownika.<br>2.Zawartość koszyka zostaje zachowana po zalogowaniu.<br>3.Wyświetlają się sekcje: 'Address Details' oraz 'Review Your Order'. |
| **TC-07** | Finalizacja zamówienia i płatności | Użytkownik jest na stronie podsumowania zamówienia ('/checkout') i jest zalogowany. | 1.Przewiń stronę w dół i kliknij przycisk **'Place order'**.<br>2.Na stronie płatności wprowadź dane z **DATA-02**.<br>3.Kliknij przycisk **'Pay and Confrim Order'**. | 1.Wyświetla się komunikat na stronie.<br>2.System umożliwia pobranie faktury(przycisk 'Download Invoice').<br>3.Uzytkownik może wrócić na stronę główną przyciskiem 'Continue'. | 
