🛒 Dokumentacja QA i Testy E2E: Automation Exercise

## 📝 O projekcie
Projekt obejmuje kompleksowe testy manualne platformy e-commerce **Automation Exercise**. Skupiłem się na weryfikacji krytycznych procesów biznesowych (Critical Business Paths), takich jak rejestracja użytkownika, zarządzanie koszykiem oraz proces płatności.

Głównym celem projektu było zaprezentowanie umiejętności projektowania dokumentacji testowej, zarządzania danymi testowymi oraz raportowania wyników w środowisku zgodnym ze standardami QA.

## 🚀 Wykorzystane narzędzia i technologie
* **Dokumentacja:** Markdown (VS 2022)
* **Zarządzanie wersjami:** Git / GitHub
* **Przeglądarka:** Google Chrome (DevTools)
* **Platforma testowa:** [Automation Exercise](https://automationexercise.com/)

## 📂 Struktura projektu
* [`TEST_CASES.md`](./TEST_CASES.md) – Pełna lista przypadków testowych (TC-01 do TC-07) z podziałem na moduły i uzasadnieniem projektowym danych.
* [`TEST_RUN_REPORT.md`](./TEST_RUN_REPORT.md) – Raport z ostatniej egzekucji testów (wszystkie testy zaliczone pomyślnie).
* [`BUG_REPORT.md`](./BUG_REPORT.md) – Szablon profesjonalnego zgłoszenia błędu wraz z analizą priorytetów i dotkliwości.

## 🧪 Zakres testów
Projekt realizuje pełny scenariusz **End-to-End (E2E)**, symulujący cykl życia klienta:
1. **Rejestracja i walidacja danych** (Happy Path & Negative Path).
2. **User Experience w koszyku** (Dodawanie produktów jako gość, utrzymanie sesji).
3. **Logika Checkoutu** (Wymuszone logowanie, weryfikacja danych adresowych).
4. **Moduł płatności** (Integracja z bramką testową, potwierdzenie zamówienia).
5. **Zarządzanie kontem** (Usunięcie konta i weryfikacja czyszczenia bazy danych).

## 💡 Kluczowe umiejętności zaprezentowane w projekcie
* Projektowanie przypadków testowych.
* Zarządzanie danymi testowymi.
* Wykonywanie testów regresji i E2E.
* Dokumentowanie wyników w profesjonalnym formacie technicznym.
* Podstawowa obsługa Git i terminala (CLI).

---
*Projekt stworzony w celach edukacyjnych jako element portfolio Junior QA.*
