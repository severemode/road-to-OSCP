
# Celem jest bycie przygotowanym na incydent i ewentualne przeciwdziałanie mu

Aby skutecznie przeciwdziałać incydentom, konieczna jest znajomość działania możliwego ataku.

Etyczni hakerzy używają tych samych technik co przestępcy, by znaleźć luki i słabości oraz ulepszać odpowiednią ochronę.

Obrońcy, znani jako **blue team**, muszą rozumieć, jak myśli atakujący, co może wybrać jako ewentualny cel i jak zwykle przebiega atak.

## Understanding Your Environment

| Pytanie obronne                        | Analogia do miasta                             | Równoważnik w bezpieczeństwie                    |
| -------------------------------------- | --------------------------------------------- | ------------------------------------------------ |
| Co chronisz? (Systemy i infrastruktura) | Domy, budynki, ludzie                         | Serwery klientów, dane, stacje robocze, użytkownicy |
| Czy widać to, co chronisz? (Widoczność) | Kamery, raporty, patrole                      | Logi, ruch sieciowy, alerty                      |
| Co klasyfikuje podejrzane zachowanie?  | Próby otwarcia zamkniętych drzwi, krążące samochody | Powtarzające się logowania, nietypowe adresy IP  |
| Jak zatrzymać zagrożenie?              | Policja, zablokowane drogi, godzina policyjna | Reguły zapory ogniowej, blokowanie adresów IP    |

## Koncepcje ochrony

Po zrozumieniu, jakie systemy działają i jak mogą być chronione, **blue team** organizuje pracę wokół listy konceptów ochrony. Te koncepty odnoszą się do każdego systemu i będą się pojawiać, jak będziesz kontynuował naukę obrony w cyberbezpieczeństwie.

### Kluczowe koncepty:

1. **Prewencja:** Wdrażanie środków bezpieczeństwa w celu zapobiegania atakom, zanim do nich dojdzie, takich jak zapory ogniowe, oprogramowanie antywirusowe i regularne aktualizacje.
2. **Detekcja:** Monitorowanie systemów i sieci w celu identyfikowania podejrzanej lub złośliwej aktywności za pomocą logów, alertów i narzędzi bezpieczeństwa.
3. **Mitygacja:** Podejmowanie działań w trakcie incydentu w celu ograniczenia szkód, takich jak blokowanie ruchu, izolowanie dotkniętych systemów lub dezaktywowanie skompromitowanych kont.
4. **Analiza:** Badanie, co się stało, jak do tego doszło i które systemy zostały dotknięte, poprzez przeglądanie logów i innych dowodów.
5. **Reakcja i poprawa:** Odbudowa po incydencie i doskonalenie środków ochrony w celu zmniejszenia ryzyka podobnych ataków w przyszłości.

**Defenderzy** nie są odpowiedzialni za ochronę wszystkiego w internecie, skupiają się na bezpieczeństwie tego, co należy do ich klienta. To na przykład urządzenia używane codziennie, serwery danych, aplikacje webowe.

## Zrozumienie systemów

Przed wdrożeniem jakichkolwiek zabezpieczeń musimy znać system, aby wiedzieć, jakie luki mogą się pojawić i jak system oddziałuje na ogólne środowisko.

### Komponenty systemu i ich ochrona

| Komponent systemu lub infrastruktury | Cel                                                                         | Analogia do miasta     |
| ----------------------------------- | --------------------------------------------------------------------------- | ---------------------- |
| Urządzenia pracowników              | Miejsca, gdzie użytkownicy pracują i mają dostęp do zasobów firmy           | Domy                   |
| Serwer WWW                          | Hostuje strony internetowe lub aplikacje, do których dostęp mają użytkownicy | Sklep/Budynki publiczne |
| Serwer pocztowy                     | Wysyła i odbiera e-maile dla organizacji                                    | Poczta                 |
| Zapora ogniowa                      | Kontroluje, jaki ruch jest dozwolony do wejścia lub wyjścia                 | Brama miasta           |
| Internet                            | Zewnętrzne sieci, które nie są kontrolowane przez organizację               | Cokolwiek poza miastem |

Jako obrońca musisz zrozumieć, jakie systemy istnieją, jak działają, jak mogą być przejęte i w jaki sposób można ograniczyć ryzyko wystąpienia incydentu do minimum.

### Zasady obrony

1. **Antycypacja zagrożeń:** Przejrzyj systemy, które chcesz chronić, i zapytaj: „Co jeśli?” Wyobraź sobie realistyczne ścieżki, którymi atakujący może podążyć, aby osiągnąć swój cel.
2. **Świadomość ataków:** Ataki zazwyczaj przebiegają w rozpoznawalnych etapach. Studiowanie typowych łańcuchów ataków i ram ochrony jest niezwykle pomocne dla obrońców.
3. **Priorytetyzacja ryzyka:** Nie każda część systemu niesie ze sobą takie samo ryzyko. Obrońcy powinni identyfikować systemy i cele o wysokiej wartości.
4. **Ciągła adaptacja:** Obrona to nie jednorazowa konfiguracja. Zagrożenia i atakujący ewoluują, techniki się zmieniają, a podatności pojawiają się na nowo.

## Dostępne narzędzia ochrony

| Komponent systemu lub infrastruktury | Co może pójść źle                                                      | Środki ochrony, które zastosujesz                                                                 |
| ------------------------------------ | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Urządzenia pracowników               | Ktoś kliknie w złośliwy link lub pobierze niebezpieczne oprogramowanie | Oprogramowanie antywirusowe do wykrywania złych programów<br>Regularne aktualizacje oprogramowania  |
| Serwer WWW                           | Atakujący próbują włamać się na stronę internetową                     | Zezwolenie tylko na bezpieczny ruch<br>Używanie bezpiecznej komunikacji                           |
| Serwer pocztowy                      | Złośliwe lub oszukańcze e-maile                                        | Filtry antyspamowe<br>Skany załączników                                                           |
| Zapora ogniowa                       | Nieznajomi z internetu próbują się włamać                              | Reguły zapory ogniowej kontrolujące dostęp<br>Blokowanie znanych "złoczyńców"                     |
| Internet zewnętrzny                  | Zewnętrzne zagrożenia pochodzą stąd                                    | Ograniczenie ruchu przychodzącego<br>Monitorowanie podejrzanej aktywności                         |

## Kluczowa terminologia

- **Zespół niebieski (Blue Team):** Grupa obrońców cyberbezpieczeństwa odpowiedzialna za ochronę systemów i reagowanie na zagrożenia.
- **Infrastruktura klienta:** Sieci, serwery, urządzenia i aplikacje należące do organizacji, które wymagają ochrony.
- **Widoczność:** Zdolność do monitorowania i obserwowania aktywności w systemach w celu wykrycia potencjalnych problemów.
- **Zagrożenie:** Potencjalne niebezpieczeństwo, takie jak hacker lub złośliwe oprogramowanie, które może zaszkodzić systemom lub danym.
- **Prewencja:** Zapobieganie zagrożeniom, zanim będą mogły wyrządzić szkody, poprzez blokowanie, ograniczanie lub zmniejszanie możliwości ataku.
- **Detekcja:** Proces identyfikowania zagrożeń lub podejrzanej aktywności w sieciach i systemach.
- **Mitygacja:** Działania podejmowane w celu zmniejszenia lub zatrzymania wpływu zagrożenia, gdy zostanie ono zidentyfikowane.
- **Ryzyko:** Prawdopodobieństwo i potencjalny wpływ zagrożenia, które skutecznie wyrządzi szkody organizacji.
