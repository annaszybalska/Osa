# Scenariusze Testowe

## User Story

**Jako** użytkownik strony Osadkowski.pl,  
**chcę** mieć informację o adresie i sposobie dostawy mojego zamówienia,  
**aby** wiedzieć gdzie i jak zostanie ono dostarczone.

## Tabela Scenariuszy Testowych

||Lista scenariuszy||Wynik oczekiwany||Weryfikacja QA||
|*SC-001 Wyświetlenie kafelka „Adres dostawy” dla zamówienia z eCommerce z dostawą do paczkomatu*| | |
|Krok 1: Zaloguj się do Osadkowski.pl jako użytkownik posiadający zamówienie eCommerce z wybraną dostawą do paczkomatu|Użytkownik jest zalogowany i ma dostęp do listy zamówień| |
|Krok 2: Otwórz szczegóły wskazanego zamówienia|Widok szczegółów zamówienia zostaje wyświetlony| |
|Krok 3: Odszukaj sekcję z informacjami o dostawie|Widoczny jest kafelek „Adres dostawy”| |
|Krok 4: Zweryfikuj treść kafelka|W kafelku prezentowane są: „Punkt odbioru: {nr paczkomatu}” oraz adres paczkomatu zgodny z danymi zamówienia| |
|*SC-002 Wyświetlenie kafelka „Adres dostawy” dla zamówienia eCommerce z dostawą na adres*| | |
|Krok 1: Zaloguj się do Osadkowski.pl jako użytkownik posiadający zamówienie eCommerce z dostawą na adres|Użytkownik jest zalogowany i ma dostęp do listy zamówień| |
|Krok 2: Otwórz szczegóły wskazanego zamówienia|Widok szczegółów zamówienia zostaje wyświetlony| |
|Krok 3: Odszukaj kafelek „Adres dostawy”|Kafelek „Adres dostawy” jest widoczny| |
|Krok 4: Zweryfikuj dane prezentowane w kafelku|Kafelek pokazuje kod pocztowy i miasto oraz linię adresową z ulicą, numerem domu i numerem mieszkania zgodne z danymi podanymi przy składaniu zamówienia| |
|*SC-003 Wyświetlenie kafelka „Adres dostawy” dla zamówienia złożonego przez PH*| | |
|Krok 1: Zaloguj się do Osadkowski.pl jako użytkownik posiadający zamówienie złożone przez PH|Użytkownik jest zalogowany i ma dostęp do listy zamówień| |
|Krok 2: Otwórz szczegóły zamówienia złożonego przez PH|Widok szczegółów zamówienia zostaje wyświetlony| |
|Krok 3: Odszukaj sekcję dostawy|Widoczny jest kafelek „Adres dostawy”| |
|Krok 4: Zweryfikuj dane kafelka zgodnie z typem dostawy zamówienia|Dla paczkomatu wyświetlane są numer i adres paczkomatu, a dla dostawy na adres wyświetlane są odpowiednie linie adresowe zgodne z zamówieniem| |
|*SC-004 Brak kafelka „Adres dostawy” dla zamówienia historycznego bez danych deliveryAddress*| | |
|Krok 1: Zaloguj się do Osadkowski.pl jako użytkownik posiadający historyczne zamówienie bez danych adresu dostawy|Użytkownik jest zalogowany i ma dostęp do listy zamówień| |
|Krok 2: Otwórz szczegóły historycznego zamówienia|Widok szczegółów zamówienia zostaje wyświetlony| |
|Krok 3: Zweryfikuj sekcję z informacjami o dostawie|Kafelek „Adres dostawy” nie jest prezentowany| |
|Krok 4: Zweryfikuj stabilność widoku szczegółów zamówienia|Brak danych adresowych nie powoduje błędu ani nieprawidłowego układu strony| |
|*SC-005 Prezentacja akcji „Ponów płatność” w kafelku „Termin płatności”*| | |
|Krok 1: Zaloguj się do Osadkowski.pl jako użytkownik posiadający zamówienie spełniające warunki do ponowienia płatności|Użytkownik jest zalogowany i ma dostęp do szczegółów zamówienia| |
|Krok 2: Otwórz szczegóły wskazanego zamówienia|Widok szczegółów zamówienia zostaje wyświetlony| |
|Krok 3: Zweryfikuj sekcję nagłówkową i kafelki informacyjne|Akcja „Ponów płatność” jest dostępna w kafelku „Termin płatności” zgodnie z założeniami funkcjonalnymi| |
|Krok 4: Zweryfikuj pozostałe kafelki nagłówka|Akcja „Ponów płatność” nie jest prezentowana w innym miejscu nagłówka| |
|*SC-006 Brak kafelka „Wartość brutto” w nagłówku szczegółów zamówienia eCare*| | |
|Krok 1: Zaloguj się do Osadkowski.pl jako użytkownik posiadający dostęp do szczegółów zamówienia w eCare|Użytkownik jest zalogowany| |
|Krok 2: Otwórz szczegóły dowolnego zamówienia objętego zmianą|Widok szczegółów zamówienia zostaje wyświetlony| |
|Krok 3: Zweryfikuj nagłówek szczegółów zamówienia|Kafelek „Wartość brutto” nie jest wyświetlany w nagłówku| |
|Krok 4: Zweryfikuj pozostałe dane nagłówka|Pozostałe wymagane informacje w nagłówku są widoczne i układ strony pozostaje poprawny| |
|*SC-007 Poprawność prezentacji linii adresowych dla dostawy na adres*| | |
|Krok 1: Zaloguj się do Osadkowski.pl jako użytkownik posiadający zamówienie z dostawą na adres, w którym dostępne są dane: ulica, numer domu/lokalu, kod pocztowy i miasto|Użytkownik jest zalogowany| |
|Krok 2: Otwórz szczegóły zamówienia|Widok szczegółów zamówienia zostaje wyświetlony| |
|Krok 3: Odszukaj kafelek „Adres dostawy”|Kafelek jest widoczny| |
|Krok 4: Porównaj treść linii adresowych z danymi źródłowymi zamówienia|Linie adresowe są zbudowane poprawnie i zawierają komplet danych adresowych w oczekiwanej kolejności, bez brakujących lub zduplikowanych elementów| |
|*SC-008 Brak jednoczesnej prezentacji paczkomatu i adresu dla jednego zamówienia*| | |
|Krok 1: Otwórz szczegóły zamówienia z dostawą do paczkomatu|Widok szczegółów zamówienia zostaje wyświetlony| |
|Krok 2: Zweryfikuj zawartość kafelka „Adres dostawy”|Prezentowane są wyłącznie dane paczkomatu, bez dodatkowych linii adresowych dla dostawy na adres| |
|Krok 3: Otwórz szczegóły zamówienia z dostawą na adres|Widok szczegółów zamówienia zostaje wyświetlony| |
|Krok 4: Zweryfikuj zawartość kafelka „Adres dostawy”|Prezentowane są wyłącznie linie adresowe dla dostawy na adres, bez informacji „Punkt odbioru”| |
