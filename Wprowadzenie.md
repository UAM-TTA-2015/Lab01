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
  * Testy weryfikujące poprawne działanie małych jednostek kodu - funkcji, rzadziej całych klas.
  Weryfikacja polega tutaj na sprawdzaniu czy dla danego stanu wejściowego kod będacy przedmiotem testu 
  "wyprodukuje" oczekiwany stan wyjściowy lub
  zakończy działanie oczekiwanym przez nas błędem. Zewnętrzne zależności zastąpione są tutaj przez 'mocki' oraz 'stuby'.
* Testy integracyjne
  * Weryfikują współpracę różnych komponentów systemu. Od testownia interakcji pomiędzy dwoma klasami do integracji z zewnętrznymi komponentam - takimi jak na przykład bazy danych.
  W przypadku testów integracyjnych, zamiast korzystać z testowych zemienników zewnętrznych zależności, wykorzystuje się ich prawdziwe implementacje.
* Testy interfejsów
  * Polegają na weryfikacji działania interfejsów będących punktami styku pomiędzy testowanym system, a użytkownikiem (wtedy interfjsem jest GUI) lub innymi systami (interfejsem jest API). 
* Testy systemowe
  * Testowanie całościowe w pełni zintegrowanego systemu mające na celu weryfikację funkcjonalnych jak i niefunkcjonalnych wymagań specyfikacji systemu.
  Nie powinny wymagać żadnej wiedzy na temat wewnętrznych szczegółów dotyczących działania testowanego systemu - tzw. black-box testing.
* Testy akceptacyjne
  * Testy wymagane w celu uzyskania potwierdzenia spełniania przez system określonego progu jakościowego - podzbiór testów systemowych.

## Typy testów
* Testy deweloperskie
  * Całość testów tworzonych przez zespół programistyczny w czasie implementacji systemu. Skupiają się na możliwie szybkim odnajdywaniu błędów, zanim  te zdołają dotrzeć do zespołu QA.
* Testy regresyjne
  * Testy mające na celu wykrycie czy we wcześniej zaimplementowanych, oddanych i przetestowanych częściach oprogramowania nie pojawiają się nowe błędy mogące być wynikem zmian konfiguracji, 
  refactoringu czy innych prac zespołu programistycznego.
* Testy eksploracyjne
  * Forma testów łącząca w sobie kilka czynności wykonywanych na raz przez zespół testerski. Łączy w sobie spontaniczną naukę działania systemu, tworzenia przypadków testowych na bazie zdobytych doświadczeń, a następnie
  odtwarzanie tych przypadków w celu zweryfikowania działania systemu.
* Testy funkcjonalne i niefunkcjonalne
  * Testy funkcjonalne w dużym uproszczeniu sprawdzają zgodność systemu z wymaganiami biznesowymi definiujący jego oczekiwane działanie - czyli CO system robi.
  * Testy niefunkcjonalne, sprawdzają JAK system to robi, czyli czy na przykład działa wydajnie, czy wytrzymuje duże obciążenie itd.
* Testy bezpieczeństwa
  * Sprawdzają czy w obszarach aplikacji takich autoryzacja, autentykacja czy dostępność nie występują błędy.
* Testy użyteczności i dostępności
  * Testy z aktywnym udziałem użytkowników aplikacji mające na celu obserwowanie ich zachowań, nawyków oraz prób przy korzystaniu z testowanego systemu.

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
  * Testy powstają razem z kodem
  * Konieczne jest dbanie o testowalność kodu – Test Driven Development to Twój przyjaciel
  * 100% pokrycie kodu testami to nie mit – co nie oznacza że zawsze jest konieczny
  * Testy odpalane są za każdym razem przed wrzuceniem zmian do repozytorium
  * Każdy build uruchamia testy
* Testy integracyjne
  * Czy komponenty potrafią się porozumieć?
  * Czy są odporne na podstawowe „czarne scenariusze”
  * Uruchamiane jak najczęściej aby szybko wykryć potencjalne problemy
* Testy interfejsów
  * Interfejsy programistyczne (API): Czy nasze usługi mają kompletne i działające API?
    * Powinny być tworzone gdy aplikacja wystawia jakiekolwiek API
  * Interfejsy użytkownika (UI): Czy nasza aplikacja ma działający interfejs użytkownika?
    * Wymagają sporego nakładu pracy, ale dobrze napisane pozwalają szybko wychwycić błędy nie wykryte przez inne rodzaje testów

### Testy manualne
* Testy eksploracyjne – odkrywają najwięcej błędów w systemie
  * Testowanie przez poznawanie - osoba przeprowadzająca test poznaje aplikację, wchodzi w różne jej części i próbuje na różne sposoby z niej korzystać.
  Może próbować wprowadzać błędne dane, zmieniać wielkość okna, ustawienia systemowe i sprawdzać jak system reaguje.
  Takie testy pozwalają na odkrycie problemów które nie są objęte standardowym zestawem testów (testy automatyczne, scenariusze testowe). 
* Testy użyteczności – sprawiają że jakość aplikacji rośnie
  * Sprawdzają czy interfejs aplikacji pozwala użytkownikowi korzystać z dostępnych funkcji bez sięgania do instrukcji, sprawdzają czy system chroni użytkownika przed popełnieniem błędów,
  czy jasno informuje gdy użytkownik popełnij jakiś błąd, itd. 
* Testy dostępności – nie każdy odbiera aplikację w ten sam sposób
  * Takie testy sprawdzają czy każdy potencjalny użytkowik systemu będzie w stanie go obsłużyć. Testowane mogą być np.:
    * Zachowanie aplikacji z różnymi ustawieniami systemu (wysoki kontrast, większe czcionki)
    * Współpraca z aplikacjami typu Screen Reader (zamiana tekstu na mowę)
* Testy akceptacyjne – czy tego właśnie potrzebuje Klient?
  * Zazwyczaj opierają się o Plan Testów (scenariusze testowe), który stworzony jest na podstawie wymagań Klienta. Weryfikują czy system dostarcza prawidłowo działające funkcjonalności opisane w wymaganiach.
* Odpal aplikację i zobacz czy działa!
  * Nie wrzucaj niczego do repozytorium zanim nie sprawdzisz czy funkcjonalność którą dodałeś działa prawidłowo i czy nie wpłynęła negatywnie na inne elementy systemu.

## Pomocne metodyki
* TDD – Test Driven Development – na poziomie testowania kodu, wymusza testowalność
* BDD – Behaviour Driven Development – na poziomie testowania wymagań
* Metodyki Agile (Scrum, Kanban, XP i inne) – krótkie cykle i częsta weryfikacja wymagań pozwalają na wcześniejsze eliminowanie błędów i minimalizowanie strat
* Dobre praktyki programowania (np. SOLID dla OOP)
* Nauka różnych języków i paradygmatów programowania
* Nauka różnych bibliotek pomocnych w testowaniu
* Code Review, programowanie w parach - wspomagają tworzenie wysokiej jakości oprogramowania

## Pomocne narzędzia i nie tylko
* Frameworki do testów jednostkowych i nie tylko - MS Test, NUnit, xUnit, FsCheck
* Frameworki do testów UI - Selenium, MS UI Automation, Gherkin, SpecFlow
* Frameworki do testów wydajnościowych - profilery, Visual Studio Testing Tools and Services
* Narzędzia do Continous Integration (CI, build server) - TeamCity, TFS, Bamboo, Jenkins
* Systemy zarządzania ticketami - Jira, Bugzilla, Mantis, GitHub, BitBucket
* Środowiska testowe (dla bardziej rozbudowanych aplikacji, np. typu klient-serwer)
* Dokumentacja wymagań - specyfikacje funkcjonalne, user story, BPMN
* Narzędzia do analizy jakościu kodu - StyleCop, FxCop, Gandarme, Sonar
* Dobre nawyki podczas tworzenia systemu - nietolerowanie warningów, ustalanie konwencji i wpólnych standardów jakościowych
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
