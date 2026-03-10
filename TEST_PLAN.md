# Plan testów: Automation Exercise (E-commerce)
**Wersja:** 1.0
**Autor:** Dawid Miotk
**Data:** 10.03.2026

---

## 1.Wstęp
Celem niniejszego dokumentu jest zdefiniowanie strategii testów dla platformy e-commerce **Automation Exercise**. Testy mają na celu zweryfikowanie kluczowych funkcjonalności sklepu,
takich jak rejestracja, zakupy, oraz proces płatności. 

## 2. Zakres testów
### 2.1. Funkcje objęte testami (In-Scope):
* **Moduł Użytkownika:** Rejestracja, logowanie, wylogowanie, usuwanie konta.
* **Moduł Produktów:** Przeglądanie listy, wyszukiwanie, filtrowanie (różne kategorie).
* **Koszyk i Zamówienia:** Dodawanie produktów, edycja ilości, proces Checkout.
* **Formularz kontaktowy:** Wysyłanie wiadomości do obsługi sklepu.

### 2.2. Funkcje wyłączone z testów (Out-of-Scope):
* Testy wydajnościowe (Load/Stress testing).
* Płatności rzeczywistymi kartami kredytowymi (używamy danych testowych).

## 3.Środowisko testowe:
* **URL:** [Strona testowa - automationexercise.com](https://automationexercise.com/)
* **Przeglądarki:** Google Chrome (najnowsza wersja)
