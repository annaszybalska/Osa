# Scenariusze Testowe

## User Story

**Jako** użytkownik systemu,  
**Chcę** móc zalogować się do aplikacji,  
**Aby** uzyskać dostęp do swoich danych i funkcjonalności systemu.

**Kryteria akceptacji:**
1. Użytkownik może zalogować się podając poprawny adres e-mail i hasło.
2. System wyświetla komunikat błędu przy podaniu niepoprawnych danych logowania.
3. Użytkownik może zresetować hasło za pomocą adresu e-mail.
4. Po 3 nieudanych próbach logowania konto zostaje tymczasowo zablokowane.
5. Zalogowany użytkownik może się wylogować.

---

## Tabela Scenariuszy Testowych

||Lista scenariuszy||Wynik oczekiwany||Weryfikacja QA||
|*SC-001 Logowanie z poprawnymi danymi*| | |
|Krok 1: Otwórz stronę logowania aplikacji|Strona logowania jest widoczna z polami: e-mail, hasło oraz przyciskiem "Zaloguj"| |
|Krok 2: Wprowadź poprawny adres e-mail zarejestrowanego użytkownika (np. test@example.com)|Pole e-mail jest uzupełnione poprawnym adresem| |
|Krok 3: Wprowadź poprawne hasło dla danego użytkownika|Pole hasło jest uzupełnione (znaki są maskowane)| |
|Krok 4: Kliknij przycisk "Zaloguj"|Użytkownik zostaje zalogowany i przekierowany na stronę główną (dashboard). Wyświetlone jest powitanie z imieniem użytkownika.| |

||Lista scenariuszy||Wynik oczekiwany||Weryfikacja QA||
|*SC-002 Logowanie z niepoprawnym hasłem*| | |
|Krok 1: Otwórz stronę logowania aplikacji|Strona logowania jest widoczna| |
|Krok 2: Wprowadź poprawny adres e-mail zarejestrowanego użytkownika|Pole e-mail jest uzupełnione| |
|Krok 3: Wprowadź niepoprawne hasło|Pole hasło jest uzupełnione| |
|Krok 4: Kliknij przycisk "Zaloguj"|System wyświetla komunikat błędu: "Nieprawidłowy adres e-mail lub hasło". Użytkownik pozostaje na stronie logowania.| |

||Lista scenariuszy||Wynik oczekiwany||Weryfikacja QA||
|*SC-003 Logowanie z niepoprawnym adresem e-mail*| | |
|Krok 1: Otwórz stronę logowania aplikacji|Strona logowania jest widoczna| |
|Krok 2: Wprowadź nieistniejący adres e-mail (np. nieznany@example.com)|Pole e-mail jest uzupełnione| |
|Krok 3: Wprowadź dowolne hasło|Pole hasło jest uzupełnione| |
|Krok 4: Kliknij przycisk "Zaloguj"|System wyświetla komunikat błędu: "Nieprawidłowy adres e-mail lub hasło". Użytkownik pozostaje na stronie logowania.| |

||Lista scenariuszy||Wynik oczekiwany||Weryfikacja QA||
|*SC-004 Logowanie z pustymi polami*| | |
|Krok 1: Otwórz stronę logowania aplikacji|Strona logowania jest widoczna| |
|Krok 2: Pozostaw pola e-mail i hasło puste|Pola są puste| |
|Krok 3: Kliknij przycisk "Zaloguj"|System wyświetla komunikaty walidacji: "Pole e-mail jest wymagane", "Pole hasło jest wymagane". Formularz nie zostaje wysłany.| |

||Lista scenariuszy||Wynik oczekiwany||Weryfikacja QA||
|*SC-005 Blokada konta po 3 nieudanych próbach logowania*| | |
|Krok 1: Otwórz stronę logowania aplikacji|Strona logowania jest widoczna| |
|Krok 2: Wprowadź poprawny e-mail i niepoprawne hasło, kliknij "Zaloguj" (1. próba)|System wyświetla komunikat błędu. Konto nie jest jeszcze zablokowane.| |
|Krok 3: Wprowadź poprawny e-mail i niepoprawne hasło, kliknij "Zaloguj" (2. próba)|System wyświetla komunikat błędu. Konto nie jest jeszcze zablokowane.| |
|Krok 4: Wprowadź poprawny e-mail i niepoprawne hasło, kliknij "Zaloguj" (3. próba)|System wyświetla komunikat: "Konto zostało tymczasowo zablokowane z powodu zbyt wielu nieudanych prób logowania. Spróbuj ponownie za 15 minut."| |
|Krok 5: Spróbuj zalogować się poprawnym hasłem w czasie blokady|System wyświetla komunikat o blokadzie konta. Logowanie nie jest możliwe.| |

||Lista scenariuszy||Wynik oczekiwany||Weryfikacja QA||
|*SC-006 Reset hasła – wysłanie e-maila resetującego*| | |
|Krok 1: Otwórz stronę logowania aplikacji|Strona logowania jest widoczna| |
|Krok 2: Kliknij link "Zapomniałem hasła"|Użytkownik zostaje przekierowany na stronę resetowania hasła z polem na adres e-mail| |
|Krok 3: Wprowadź adres e-mail zarejestrowanego użytkownika|Pole e-mail jest uzupełnione| |
|Krok 4: Kliknij przycisk "Wyślij link resetujący"|System wyświetla komunikat: "Link do resetowania hasła został wysłany na podany adres e-mail." Wiadomość e-mail z linkiem zostaje dostarczona.| |

||Lista scenariuszy||Wynik oczekiwany||Weryfikacja QA||
|*SC-007 Wylogowanie z aplikacji*| | |
|Krok 1: Zaloguj się do aplikacji poprawnymi danymi|Użytkownik jest zalogowany i widzi stronę główną| |
|Krok 2: Kliknij ikonę/menu użytkownika w prawym górnym rogu|Pojawia się menu z opcją "Wyloguj"| |
|Krok 3: Kliknij opcję "Wyloguj"|Użytkownik zostaje wylogowany i przekierowany na stronę logowania. Sesja użytkownika zostaje zakończona.| |
|Krok 4: Spróbuj cofnąć się w przeglądarce (przycisk "Wstecz")|Użytkownik nie ma dostępu do chronionych stron – zostaje przekierowany z powrotem na stronę logowania.| |
