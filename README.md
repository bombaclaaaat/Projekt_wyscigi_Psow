1.Instalacja i konfiguracja środowiska
    Instalacja frameworka Laravel, PHP oraz niezbędnego oprogramowania do tworzenia strony.
    Przygotowanie środowiska programistycznego, które umożliwi efektywną pracę nad projektem.
2.Pomysł na projekt
    Główny temat projektu: wyścigi psów.
    Opracowanie szczegółowych założeń, takich jak funkcjonalności strony i jej główne elementy.
3.Tworzenie modeli, migracji i tras
    Implementacja modeli, migracji oraz tras (routes) wymaganych do działania strony internetowej.
    Zapewnienie zgodności struktury aplikacji z założeniami projektu.
4.Konfiguracja Vite 
    Dostosowanie pliku vite.config w celu ustawienia poprawnej ścieżki wczytywania strony.
5.Budowa bazy danych
    Utworzenie bazy danych w formacie SQLite.
    Zaimplementowanie struktury przechowującej dane użytkowników oraz ich ról, co umożliwia kontrolę dostępu do różnych części strony.
6.Testowanie strony
    Przeprowadzenie pierwszych testów funkcjonalnych w celu sprawdzenia poprawności działania aplikacji.
7.Tryb dla osób z niepełnosprawnościami
    Dodanie funkcji wysokiego kontrastu, aby strona była bardziej dostępna dla osób z problemami wzrokowymi.
8.Poprawki logowania i ról użytkowników
    Udoskonalenie mechanizmu logowania.
    Poprawienie logiki zarządzania rolami użytkowników, aby odpowiednio sterować widocznością treści na stronie.
9.Końcowe testy
    Przeprowadzenie szczegółowych testów, w tym:
    Próby usuwania i dodawania rekordów zarówno z poziomu interfejsu strony, jak i w terminalu (CMD).
    Sprawdzenie funkcjonalności strony pod kątem technicznym.
    Testowanie dodatkowych efektów i funkcji aplikacji.

PIES

    Opis: Tabela przechowująca informacje o psach biorących udział w wyścigach.
    Zawartość:
    ID psa
    Imię
    Wiek
    Identyfikator rasy (powiązanie z tabelą RASA)
    Właściciel (powiązanie z tabelą WLASCICIEL)
    Cel: Reprezentuje poszczególne psy uczestniczące w wyścigach. Każdy rekord to unikalny pies, który może być przypisany do różnych wyścigów.
RASA

    Opis: Tabela przechowująca dane o rasach psów.
    Zawartość:
    ID rasy
    Nazwa rasy
    Charakterystyka rasy (opcjonalne, np. szybkość, wytrzymałość)
    Cel: Umożliwia kategoryzację psów według ras, co pozwala na różnorodność uczestników wyścigów i ewentualne statystyki.
SPONSOR

    Opis: Tabela przechowująca dane sponsorów wspierających wyścigi.
    Zawartość:
    ID sponsora
    Nazwa firmy
    Kontakt
    Kwota wsparcia lub rodzaj wsparcia (np. nagrody, promocja)
    Cel: Ułatwia zarządzanie sponsorami i ich wkładem w organizację wyścigów.
TOR WYŚCIGOWY

    Opis: Tabela opisująca tory wyścigowe, na których odbywają się zawody.
    Zawartość:
    ID toru
    Nazwa toru
    Lokalizacja
    Długość toru
    Cel: Zapewnia dane o miejscach, gdzie organizowane są wyścigi, co pozwala na planowanie i organizację zawodów.
USER

    Opis: Tabela użytkowników serwisu.
    Zawartość:
    ID użytkownika
    Nazwa użytkownika
    E-mail
    Hasło
    Rola (np. admin, widz, właściciel psa)
    Cel: Zarządza dostępem do różnych funkcjonalności strony w zależności od roli użytkownika.
WLASCICIEL

    Opis: Tabela przechowująca dane właścicieli psów.
    Zawartość:
    ID właściciela
    Imię i nazwisko
    Kontakt
    Cel: Umożliwia powiązanie psów z ich właścicielami, co jest kluczowe przy zgłaszaniu ich do wyścigów.
WYNIK

    Opis: Tabela przechowująca wyniki wyścigów.
    Zawartość:
    ID wyniku
    ID psa (powiązanie z tabelą PIES)
    ID wyścigu (powiązanie z tabelą WYSCIG)
    Pozycja na mecie
    Czas ukończenia
    Cel: Rejestruje wyniki każdego psa w wyścigach, co pozwala na analizę i porównania osiągnięć.
WYSCIG

    Opis: Tabela opisująca wyścigi jako wydarzenia.
    Zawartość:
    ID wyścigu
    Data i godzina
    ID toru (powiązanie z tabelą TOR WYŚCIGOWY)
    Nazwa wyścigu
    Cel: Zarządza danymi o poszczególnych wyścigach, co pozwala na planowanie i zapisy wyników.
ZGLOSZENIE

    Opis: Tabela przechowująca zgłoszenia psów do wyścigów.
    Zawartość:
    ID zgłoszenia
    ID psa (powiązanie z tabelą PIES)
    ID wyścigu (powiązanie z tabelą WYSCIG)
    Data zgłoszenia
    Cel: Umożliwia zarządzanie uczestnikami wyścigów poprzez przypisywanie psów do konkretnych zawodów.
