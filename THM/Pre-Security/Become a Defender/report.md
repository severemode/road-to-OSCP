Celem jest bycie przygotowanym na incydent i ewnetualne przeciwdzialanie mu, potrzebna jest do tego znajomosc dzialania mozliwego ataku.

Etyczni hakerzy uzywaja takich samych technik jak przestepcy by znalezc luki i slabosci oraz ulepszac odowiednia ochrone

Obroncy, znani jako blue team, musza rozumiec jak mysli atakujacy, co moze wybrac jako ewentualny cel i jak zwykle przebiega atak


Understanding Your Environment


| Pytanie obronne                         | Analogia do miasta                                  | Równoważnik w bezpieczeństwie                       |
| --------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| Co chronisz? (Systemy i infrastruktura) | Domy, budynki, ludzie                               | Serwery klientów, dane, stacje robocze, użytkownicy |
| Czy widać to, co chronisz? (Widoczność) | Kamery, raporty, patrole                            | Logi, ruch sieciowy, alerty                         |
| Co klasyfikuje podejrzane zachowanie?   | Próby otwarcia zamkniętych drzwi, krążące samochody | Powtarzające się logowania, nietypowe adresy IP     |
| Jak zatrzymać zagrożenie?               | Policja, zablokowane drogi, godzina policyjna       | Reguły zapory ogniowej, blokowanie adresów IP       |



Jak juz zrozumiesz jakie systemy dzialaja i jak moga byc chronione, blue team zwykle organizuje prace wokol listy konceptow ochrony. Te koncepty odnosza sie do kazdego systemu i beda sie pojawiac ciagle jak bedziesz kontynuowal nauke defencywnego cybersec.

1.Prewencja: Wdrażanie środków bezpieczeństwa w celu zapobiegania atakom, zanim do nich dojdzie, takich jak zapory ogniowe, oprogramowanie antywirusowe i regularne aktualizacje.

2.Detekcja: Monitorowanie systemów i sieci w celu identyfikowania podejrzanej lub złośliwej aktywności za pomocą logów, alertów i narzędzi bezpieczeństwa.

3.Mitygacja: Podejmowanie działań w trakcie incydentu w celu ograniczenia szkód, takich jak blokowanie ruchu, izolowanie dotkniętych systemów lub dezaktywowanie skompromitowanych kont.

4.Analiza: Badanie, co się stało, jak do tego doszło i które systemy zostały dotknięte, poprzez przeglądanie logów i innych dowodów.

5.Reakcja i poprawa: Odbudowa po incydencie i doskonalenie środków ochrony w celu zmniejszenia ryzyka podobnych ataków w przyszłości.



defenders nie sa odpowiedzialni za ochrone wszystkiego w internecie, skupiaja sie na bezpieczenstwie tego co nalezy do ich klienta. To na przyklad urzadzenia uzywane codziennie, serwery danych, web. Przed wdrozeniem jakichkolwiek zabezpieczen, musimy znac system aby wiedziec jakie luki moga sie pojawic i w jaki system oddzialowuje na ogolne srodowisko !.

| Komponent systemu lub infrastruktury | Cel                                                                          | Analogia do miasta      |
| ------------------------------------ | ---------------------------------------------------------------------------- | ----------------------- |
| Urządzenia pracowników               | Miejsca, gdzie użytkownicy pracują i mają dostęp do zasobów firmy            | Domy                    |
| Serwer WWW                           | Hostuje strony internetowe lub aplikacje, do których dostęp mają użytkownicy | Sklep/Budynki publiczne |
| Serwer pocztowy                      | Wysyła i odbiera e-maile dla organizacji                                     | Poczta                  |
| Zapora ogniowa                       | Kontroluje, jaki ruch jest dozwolony do wejścia lub wyjścia                  | Brama miasta            |
| Internet                             | Zewnętrzne sieci, które nie są kontrolowane przez organizację                | Cokolwiek poza miastem  |


Jako obronca musisz zrozumiec jakie systemy istnieja, jak dzialaja, jak moga byc przejete i w jaki sposob mozna ograniczyc ryzyko wystapienia incydentu do minimum.


Nalezy patrzec na swoje system jako lancuch polaczonych ze soba narzedzi, co moze sie stac w jednej co ma wplyw na druga. Atatkujacy rzadko wykorzystuja dzire tylko w jednej technologii. 

Kluczowe zasady obrony:

1.Antycypacja zagrożeń: Przejrzyj systemy, które chcesz chronić, i zapytaj: „Co jeśli?” Wyobraź sobie realistyczne ścieżki, którymi atakujący może podążyć, aby osiągnąć swój cel.

2.Świadomość ataków: Ataki zazwyczaj przebiegają w rozpoznawalnych etapach. Studiowanie typowych łańcuchów ataków i ram ochrony jest niezwykle pomocne dla obrońców.

3.Priorytetyzacja ryzyka: Nie każda część systemu niesie ze sobą takie samo ryzyko. Obrońcy powinni identyfikować systemy i cele o wysokiej wartości.

4.Ciągła adaptacja: Obrona to nie jednorazowa konfiguracja. Zagrożenia i atakujący ewoluują, techniki się zmieniają, a podatności pojawiają się na nowo.



Dostepne obrony, narzedzia do ochrony:

| Komponent systemu lub infrastruktury | Co może pójść źle                                                      | Środki ochrony, które zastosujesz                                                                  |
| ------------------------------------ | ---------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| Urządzenia pracowników               | Ktoś kliknie w złośliwy link lub pobierze niebezpieczne oprogramowanie | Oprogramowanie antywirusowe do wykrywania złych programów<br>Regularne aktualizacje oprogramowania |
| Serwer WWW                           | Atakujący próbują włamać się na stronę internetową                     | Zezwolenie tylko na bezpieczny ruch<br>Używanie bezpiecznej komunikacji                            |
| Serwer pocztowy                      | Złośliwe lub oszukańcze e-maile                                        | Filtry antyspamowe<br>Skany załączników                                                            |
| Zapora ogniowa                       | Nieznajomi z internetu próbują się włamać                              | Reguły zapory ogniowej kontrolujące dostęp<br>Blokowanie znanych "złoczyńców"                      |
| Internet zewnętrzny                  | Zewnętrzne zagrożenia pochodzą stąd                                    | Ograniczenie ruchu przychodzącego<br>Monitorowanie podejrzanej aktywności                          |





**Kluczowa terminologia**

* **Zespół niebieski (Blue Team):** Grupa obrońców cyberbezpieczeństwa odpowiedzialna za ochronę systemów i reagowanie na zagrożenia.
* **Infrastruktura klienta:** Sieci, serwery, urządzenia i aplikacje należące do organizacji, które wymagają ochrony.
* **Widoczność:** Zdolność do monitorowania i obserwowania aktywności w systemach w celu wykrycia potencjalnych problemów.
* **Zagrożenie:** Potencjalne niebezpieczeństwo, takie jak hacker lub złośliwe oprogramowanie, które może zaszkodzić systemom lub danym.
* **Prewencja:** Zapobieganie zagrożeniom, zanim będą mogły wyrządzić szkody, poprzez blokowanie, ograniczanie lub zmniejszanie możliwości ataku.
* **Detekcja:** Proces identyfikowania zagrożeń lub podejrzanej aktywności w sieciach i systemach.
* **Mitygacja:** Działania podejmowane w celu zmniejszenia lub zatrzymania wpływu zagrożenia, gdy zostanie ono zidentyfikowane.
* **Ryzyko:** Prawdopodobieństwo i potencjalny wpływ zagrożenia, które skutecznie wyrządzi szkody organizacji.
