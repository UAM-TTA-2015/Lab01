# Wprowadzenie do testowania

## Jak nasza aplikacja się rozrasta
* Wyrażenia
* Instrukcje
* Funkcje / Metody
* Klasy / Moduły
* Biblioteki / Aplikacje
* Systemy

## Problemy z rozrastającymi się aplikacjami
* Rosnąca liczba funkcji i zależności pomiędzy nimi
* Zmieniające się wymagania
* Zmieniające się koncepcje
* Różne środowiska, platformy, zróżnicowani Klienci

## Co zyskam testując aplikację
* Wyższą jakość aplikacji i jej kodu
* Ułatwiony refactoring
* Zadowolonego Klienta
* Wiele spokojnych nocy
* Uznanie i wieczną chwałę od obecnych i przyszłych kolegów
* Mnóstwo czasu i pieniędzy!

## Poziomy testów
* Testy jednostkowe
  * TODO
* Testy integracyjne
  * TODO
* Testy interfejsów
  * TODO
* Testy systemowe
  * TODO
* Testy akceptacyjne
  * TODO

## Typy testów
* Testy deweloperskie
  * TODO
* Testy regresyjne
  * TODO
* Testy eksploracyjne
  * TODO
* Testy funkcjonalne i niefunkcjonalne
  * TODO
* Testy wydajnościowe
  * TODO
* Testy bezpieczeństwa
  * TODO
* Testy użyteczności i dostępności
  * TODO
* ...

## Co testować?
* Wszystko! A tak na prawdę...
* Wymagania Klienta
* Zgodność aplikacji z wymaganiami Klienta
* Kluczowe komponenty aplikacji
* Logikę aplikacji
* Najczęściej wykorzystywane funkcje
* Integralność systemu
* Komunikację pomiędzy komponentami
* Komunikację z zewnętrznymi systemami
* Komunikację z Użytkownikiem
* Bezpieczeństwo systemu
* Wydajność systemu
* ...

## Jak testować?

### Testy zautomatyzowane
* Testy jednostkowe
  * Dbanie o testowalność kodu – Test Driven Development to Twój przyjaciel
  * 100% code coverage to nie mit – co nie oznacza że zawsze jest konieczny
  * TODO
* Testy integracyjne
  * Czy komponenty potrafią się porozumieć?
  * Czy są odporne na podstawowe „czarne scenariusze”
  * TODO
* Testy interfejsów
  * Interfejsy programistyczne (API): Czy nasze usługi mają kompletne i działające API?
  * Interfejsy użytkownika (UI): Czy nasza aplikacja ma działający interfejs użytkownika?
  * TODO

### Testy manualne
* Testy eksploracyjne – odkrywają najwięcej błędów w systemie
  * TODO
* Testy użyteczności – sprawiają że jakość aplikacji rośnie
  * TODO
* Testy dostępności – nie każdy odbiera aplikację w ten sam sposób
  * TODO
* Testy akceptacyjne – czy tego właśnie potrzebuje Klient?
  * TODO
* Odpal aplikację i zobacz czy działa!
  * TODO

## Pomocne metodyki
* TDD – Test Driven Development – na poziomie testowania kodu, wymusza testowalność 
* BDD – Behaviour Driven Development – na poziomie testowania wymagań
* Metodyki Agile (Scrum, Kanban, XP i inne) – krótkie cykle i częsta weryfikacja wymagań pozwalają na wcześniejsze eliminowanie błędów i minimalizowanie strat
* Dobre praktyki programowania (np. SOLID dla OOP)
* Nauka różnych języków i paradygmatów programowania
* TODO

## Pomocne narzędzia i nie tylko
* Frameworki do testów jednostkowych i nie tylko - MS Test, NUnit, xUnit, FsCheck
* Frameworki do testów UI - Selenium, MS UI Automation, Gherkin, SpecFlow
* Frameworki do testów wydajnościowych - TODO
* Narzędzia do Continous Integration (CI, build server) - TeamCity, TFS, Bamboo, Jenkins, 
* Systemy zarządzania ticketami - Jira, Bugzilla, Mantis, GitHub, BitBucket
* Środowiska testowe (dla bardziej rozbudowanych aplikacji, np. typu klient-serwer)
* Dokumentacja wymagań - specyfikacje funkcjonalne, user story, TODO
* Narzędzia do analizy jakościu kodu - StyleCop, FxCop, Gandarme, Sonar 
* Dobre nawyki podczas tworzenia systemu - TODO
* Specjaliści od QA (Quality Assurance - testerzy) w zespole
* Dobra komunikacja i współpraca z Klientem

## Gdy czas nas goni...

### Z czego nie rezygnować
* Nie rezygnuj z testowania
* Nie rezygnuj z testowania kluczowej logiki aplikacji
* Nie rezygnuj z uwzględniania testów w wycenie aplikacji
* Nie rezygnuj z pisania testowalnego kodu

### Gdy trzeba ciąć zakręty...
* Skup się na kluczowych aspektach aplikacji
* Pomiń skrajne (mało prawdopodobne) przypadki
* Dostosuj ilość automatycznych testów do możliwości czasowych / budżetowych
* Działająca aplikacja z mniejszym pokryciem testami jest lepsza niż niedziałająca z 100% pokryciem...
* ...z drugiej strony lepiej dostarczyć mniej funkcji wysokiej jakości niż więcej niedokończonych
