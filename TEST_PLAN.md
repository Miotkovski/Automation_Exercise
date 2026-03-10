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

## 3.Środowisko testowe
* **URL:** [Strona testowa - automationexercise.com](https://automationexercise.com/)
* **Przeglądarki:** Google Chrome (najnowsza wersja)
* **Urządzenia:** Desktop (Windows) oraz emulacja urządzenia mobilnego (DevTools).

## 4. Strategia testów
* **Typy testów:** * Testy funkcjonalne (Manualne).
    * Testy regresji (po zgłoszeniu porawek).
    * Testy dymne (Smoke tests) - kluczowe ścieżki po każdym wdrożeniu.
    * Testy UI/UX - zgodność interfejsu z intuicyjną nawigacją.
* **Podejście:** Black-box (brak wglądu w kod źródłowy).

## 5.Narzędzia
* **Zarządzanie testami:** GitHub (Issues & Projects).
* **Raportowanie błędów:** Jira / Github Issues.
* **Testy API:** Postman.
* **Dokumentacja:** Markdown.

## 6.Kryteria akceptacji
* **Kryterium wejścia/rozpoczęcia:** Dostępność stabilnej wersji strony na serwerze testowym
* **Kryteria wyjścia/zakończenia:** * Wykonanie 100% zaplanowanych przypadków testowych.
    * Brak błędów o priorytecie "Blocker" i "Critical".
 
## 7.Analiza Ryzyk 
| Ryzyko | Poziom | Plan mitygacji |
| :--- | :--- | :--- |
| Problemy z dostepnością serwera | Średni 🟠 | Powtórzenie testów po przywróceniu stabilności. |
| Reklamy Google Ads przesłaniające UI | Niski 🟢 | Użycie adBlocka podczas testów funkcjonalnych. |

---

