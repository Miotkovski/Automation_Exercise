# Przypadki testowe: Automation Exercise

## 1. Moduł: Rejestracja i Zarządzanie Kontem

> ** Notatka techniczna: ** > Przypadki testowe w module Rejestracji zostały zaprojektowane jako **scenariusz zależny**. <br>
> Zestaw 'DATA-01' jest celowo współdzielony między TC-01 a TC-02

## 🪪 Dane Testowe (Test data Pool)
| ID Danych | Imię / Nazwisko | E-mail | Hasło | Szczegóły (Płeć, Data ur. Adres, nr telefonu) | Company | Checkboxy | 
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **DATA-01** | Jan QA | tester_jan@poczta.pl | Pasword123 | Pan, **12/05/1990**, <br>USA, California, Los Angeles, <br>Sezamkowa 10, 90001, <br>123456789 | Test Company | Newsletter: TAK, Offers: TAK |
<br>
<br>


| ID | Tytuł | Warunki testowe | Kroki testowe | Oczekiwany rezultat |
| :--- | :--- | :--- | :---| :--- |
| **TC-01** | Skuteczna rejestracja nowego użytkownika | Użytkownik nie posiada konta na platformie | 1. Wejdź na stronę główną. <br>2. Kliknij przycisk 'Sign Up' / Login<br>3. W sekcji 'New User Signup!' wprowadź dane(**DATA-01**).<br>4. Kliknij 'Signup'.<br>5. Wypełnij formularz (**DATA-01).<br>6. Kliknij 'Create Account'. | Wyświetla się komunikat: 'ACCOUNT CREATED!' oraz przycisk 'Continue'.|
| **TC-02** | Próba rejestracji na istniejący e-mail | Istnieje jużkonto zarejestrowane na e-mail: 'test@test.com' | 1. Wejdź na stronę 'Signup / Login'<br>2. Wpisz nazwę i e-mail: 'test@test.com'.<br>3. Kliknij 'Signup'. | Pojawia się komunikat o błędzie: 'Email Address already exist'. |
| **TC-03** | Usunięcie konta użytkownika | Użytkownik jest zalogowany na swoje konto. | 1.Kliknij przycisk 'Delete Account.<br> 2. Konto zostaje usunięte. | Wyświetla się komunikat 'ACCOUNT DELETED!'. |
| **TC-04** | Dodanie produktu do koszyka jako Gość | 1.Użytkownik nie jest zalogowany.<br>2.Koszyk jest pusty. | 1.Wejdź na stronę główną [Automation Exercise](https://automationexercise.com)<br>2.Przewiń w dół do sekcji **'Features Items'**.<br>3.Najedź myszką na pierwszy dostępny produkt (np.'Blue Top') i kliknij **'Add to cart'**.<br>4.W oknie modalnym (pop-up), które się pojawi, kliknij przycisk **'View Cart'** | 1.Użytkownik zostaje przekierowany do widoku koszyka ('/view__cart')<br>2.Produkt 'Blue Top' jest widoczny na liście.<br>3.Ilość (Quantity) wynosi 1, a cena zgadza się z ceną na stronie głównej.<br>4.Użytkownik nie został poproszony o logowanie na tym etapie. |
| **TC-05** | Próba przejścia do płatności (Checkout) jako Gość |1. Użytkownik nie jest zalogowany.<br>2.W koszyku znajduje się conajmniej jeden produkt.| 1.Przejdź do widoku koszyka ('/view_cart').<br>2.Kliknij przycisk **'Proceed To Checkout'**. | 1.Pojawia się okno modalne (pop-up) z komunikatem: 'Checkout: Register / Login to proceed checkout'.<br>2.Użytkownik widzie dwie opcjeL 'Register/Login' oraz 'Continue On Cart'.<br>3.System **nie pozwala** na przejście do strony z danymi wysyłki bez założenia konta(strona '/checkout') nie powinna się załadować. |
| **TC-06** | Próba przejścia do checkout po rejestracji (User flow) | Użytkownik jest w widoku ('/view_cart') jako Gość.<br>W koszyku znajduje się produkt. | 1.Kliknij przycisk **'Proceed To Checkout'**.<br>2.W oknie modalnym (pop-up) kliknij link **'Register / Login'**.<br>3.Przejdź pełny proces rejestracji (jak w TC-01).<br>4.Po ukończeniu rejestracji i kliknięciu 'Continue', wróć do koszyka i ponownie kliknij **'Proceed To Checkout'**. | System "zapamiętał" zawartość koszyka po procesie rejestracji.<br>Po kliknięciu 'Proceed To Checkout' (już zalogowany) użytkownik zostaje przekierowany do strony podsumowującej zamówienie ('/checkout')<br>Wyświetlają się sekcje: 'Address Details' oraz 'Review Your Order'. |

## Raport z wykonania testów (Data: 2026-03-14)

| ID | Tytuł | Status | Uwagi | 
| :--- | :--- | :--- | :--- |
|**TC-01** | 