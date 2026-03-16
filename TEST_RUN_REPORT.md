# Raport z wykonania testów 

**Data:** 14.03.2026
**Środowisko:** Production (https://automationexercise.com/)
**Przeglądarka:** Chrome v146
**Tester:** Dawid Miotk

## Podsumowanie
* **Wszystkie testy:** 6
* **Zaliczone testy:** 1
* **Błędy:** 0
* **Oczekujące:** 5

##Szczegółowe wyniki
| ID | Tytuł | Status | Uwagi |
| :--- | :--- | :--- | :--- |
| **TC-01** | Skuteczna rejestracja | 🟩 PASSED | Użyto zestawu danych DATA-01. Formularz zaakceptował dane bez błędów. |
| **TC-02** | Rejestracja na istniejący e-mail | 🟩 PASSED | Użyto zestawu danych DATA-01. Wyświetlił się komunikat "Email Address already exist!" |
| **TC-03** | Usunięcie użytkownika | ⏳ PENDING |  |
| **TC-04** | Dodanie produktu jako Gość | 🟩 PASSED | Pomyślnie dodano produkt do pustego koszyka. Nie wyświetlił się komunikat o żądaniu logowania |
| **TC-05** | Blokada płatności dla Gościa | 🟩 PASSED | Okno pop-up wyświetla się poprawnie. System nie pozwala na przejście do strony z danymi wysyłki. |
| **TC-06** | Powrót do checkout po logowaniu | 🟩 PASSED | System pomyślnie loguje użytkownika. Zawartość koszyka pozostaje w stanie z przed logowania(1 przedmiot). Wyświetlają się sekcje dot. danych wysyłkowych oraz przeglądu koszyka. |
| **TC-07** | Finalizacja zamówienia i płatności | 🟩 PASSED | Poprawne przekierowanie do strony płatności. Płatność przebiegła pomyślnie. |