Whats offensive security?


Offensive Security focuses on proactively testing systems by attempting to break into them, with  a goal of identifying weaknesses before real attackers can exploit them.


Red Teaming:
Ustrukturyzowana, autoryzowana metoda symulowanego ataku, której celem jest odwzorowanie działań rzeczywistego przeciwnika w celu przetestowania skuteczności mechanizmów obronnych oraz wykrycia podatności w określonym zakresie.

Test penetracyjny (Penetration Test):
Ustrukturyzowana ocena bezpieczeństwa, w której uprawniony tester próbuje zidentyfikować i wykorzystać podatności w określonym zakresie, aby ocenić realny poziom ryzyka.

Podatność (Vulnerability):
Słabość lub błąd w systemie, aplikacji albo konfiguracji, który może zostać wykorzystany przez atakującego.

Eksploit (Exploit):
Technika lub metoda wykorzystania podatności w celu osiągnięcia określonego rezultatu, na przykład uzyskania nieautoryzowanego dostępu do funkcji systemu lub danych.

Zakres (Scope):
Granice określające, co może być testowane w ramach danego zlecenia. Zakres definiuje, które systemy, aplikacje i działania są dozwolone, a które pozostają poza testem.



[Działanie]

mamy strone web o url http://www.onlineshop.thm/

na poczatku sprawdzmy czy posiada jakies ciekawe podstrony,mozemy zrobic to na poczatku recznie dla podstawowych.

/admin, /login, /register, /sitemap

w tym przypadku znaleziono strone /login, sprwadzmy podstawowe hasla - user: admin passwd: qwerty

Automated Tools:

GoBuster - to narzędzie umożliwia nam automatyczne przskanowanie strony pod względem dostępnych podstron:

gobuster dir --url http://www.onlineshop.thm/ -w /usr/share/wordlists/dirbuster/directory-list.txt

dir
Tryb enumeracji katalogów i plików, który próbuje odnaleźć ukryte katalogi oraz pliki na serwerze WWW.

--url http://www.onlineshop.thm/
Określa docelową stronę internetową, którą Gobuster będzie skanował.

-w /usr/share/wordlists/dirbuster/directory-list.txt
Wskazuje listę słów (wordlist), której Gobuster użyje do odgadywania nazw katalogów i plików.




Eksploitacja slabosci

Aby zostac etycznym hackerem musisz myslec jak prawdziwy haker. Hacker probuje zrozumiec czy dany produkt czy funckjonalnosc dziala w odpowiedni sposob i co mozna zrobic jesli tak nie dziala.

Tu kilka kluczowych pytań które można miec na uwadze podczas dalszej drogi.

1. Zadawaj pytania, nie zakladaj ze cos dziala na pewno. Pomyśl, "co jeśli coś nie działa tak jak zaplanował autora i co moge dzięki temu zyskać"
2. Testuj niespodziewane: sprobuj akcji ktorych odpowiedniej obslugi developer mogl nie zaimplementowac.
3. Łącz zę sobą małe słabości. Mała podatność może samotnie dużo nie zmieniać, ale w polaczeniu z innymi moze stworzyc wieksze mozliwosci
4. Myśl jak przęstępca. "Jak cybeprzestepca podszedlby do tematu"


WAŻNE CELE:

1.Sensitive functionality (Funkcjonalności wrażliwe)
To części systemu, które wykonują krytyczne operacje, np. modyfikacja danych, dostęp do treści prywatnych, uruchamianie procesów systemowych.

2.Jeśli atakujący uzyska do nich dostęp, może wyrządzić realne szkody.
User data (Dane użytkowników)

3.Informacje osobiste, np. imiona, e-maile, hasła, dane kont.
Mogą zostać wykradzione, sprzedane lub wykorzystane do dalszych ataków (np. phishing).

4.Administrative features (Funkcje administracyjne)
Funkcje z wysokimi uprawnieniami, np. zarządzanie użytkownikami, zmiana konfiguracji, pełna kontrola nad aplikacją.
Dostęp do nich daje atakującemu niemal pełną władzę nad systemem.

5.Further attack opportunities (Dalsze możliwości ataku)
Gdy atakujący uzyska autoryzowany dostęp, może wykorzystać inne luki w aplikacji, np. do eskalacji uprawnień, poruszania się w sieci wewnętrznej lub przejęcia kolejnych kont.
