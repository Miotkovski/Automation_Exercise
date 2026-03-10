# Przypadki testowe: Automation Exercise

## 1. Moduł: Rejestracja i Zarządzanie Kontem
| ID | Tytuł | Warunki testowe | Kroki testowe | Oczekiwany rezultat |
| :--- | :--- | :--- | :---| :--- |
| **TC-01** | Skuteczna rejestracja nowego użytkownika | Użytkownik nie posiada konta na platformie | 1. Wejdź na stronę główną. <br>2. Kliknij przycisk 'Sign Up' / Login<br>3. W sekcji 'New User Signup!' wpisz Imię i poprawny e-mail.<br>4. Kliknij 'Signup'.<br>5. Wypełnij formularz (Hasło, Dane adresowe).<br>6. Kliknij 'Create Account'. | Wyświetla się komunikat: 'ACCOUNT CREATED!' oraz przycisk 'Continue'.|
| **TC-02** | Próba rejestracji na istniejący e-mail | Istnieje jużkonto zarejestrowane na e-mail: 'test@test.com' | 1. Wejdź na stronę 'Signup / Login'<br>2. Wpisz nazwę i e-mail: 'test@test.com'.<br>3. Kliknij 'Signup'. | Pojawia się komunikat o błędzie: 'Email Address already exist'. |
