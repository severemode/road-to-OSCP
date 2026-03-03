# Offensive Security

Offensive Security focuses on proactively testing systems by attempting to break into them, with a goal of identifying weaknesses before real attackers can exploit them.

## Red Teaming:
Ustrukturyzowana, autoryzowana metoda symulowanego ataku, której celem jest odwzorowanie działań rzeczywistego przeciwnika w celu przetestowania skuteczności mechanizmów obronnych oraz wykrycia podatności w określonym zakresie.

## Test penetracyjny (Penetration Test):
Ustrukturyzowana ocena bezpieczeństwa, w której uprawniony tester próbuje zidentyfikować i wykorzystać podatności w określonym zakresie, aby ocenić realny poziom ryzyka.

## Podatność (Vulnerability):
Słabość lub błąd w systemie, aplikacji albo konfiguracji, który może zostać wykorzystany przez atakującego.

## Eksploit (Exploit):
Technika lub metoda wykorzystania podatności w celu osiągnięcia określonego rezultatu, na przykład uzyskania nieautoryzowanego dostępu do funkcji systemu lub danych.

## Zakres (Scope):
Granice określające, co może być testowane w ramach danego zlecenia. Zakres definiuje, które systemy, aplikacje i działania są dozwolone, a które pozostają poza testem.

---

## Przykład: Testowanie strony www

**URL:** http://www.onlineshop.thm/

Na początek sprawdzamy, czy strona posiada jakieś ciekawe podstrony. Możemy zrobić to ręcznie, sprawdzając:

- `/admin`
- `/login`
- `/register`
- `/sitemap`

W tym przypadku znaleziono stronę `/login`. Sprawdzamy podstawowe hasła:

- **user:** admin
- **passwd:** qwerty

### Narzędzia automatyczne:

#### GoBuster

To narzędzie umożliwia nam automatyczne skanowanie strony pod względem dostępnych podstron:

```bash
gobuster dir --url http://www.onlineshop.thm/ -w /usr/share/wordlists/dirbuster/directory-list.txt

"dir": Tryb enumeracji katalogów i plików, który próbuje odnaleźć ukryte katalogi oraz pliki na serwerze WWW
.

--url http://www.onlineshop.thm/: Określa docelową stronę internetową, którą Gobuster będzie skanował.

-w /usr/share/wordlists/dirbuster/directory-list.txt: Wskazuje listę słów (wordlist), której Gobuster użyje do odgadywania nazw katalogów i plików.

## Eksploitacja słabości

Aby zostać etycznym hackerem, musisz myśleć jak prawdziwy haker. Haker próbuje zrozumieć, czy dany produkt lub funkcjonalność działa w odpowiedni sposób i co można zrobić, jeśli tak nie jest.

### Kluczowe pytania do rozważenia:

1. **Zadawaj pytania** – nie zakładaj, że coś działa na pewno. Pomyśl: "Co jeśli coś nie działa tak, jak zaplanował autor i co mogę zyskać?"
2. **Testuj niespodziewane** – spróbuj akcji, których odpowiedniej obsługi developer mógł nie zaimplementować.
3. **Łącz małe słabości** – mała podatność może samotnie niewiele zmieniać, ale w połączeniu z innymi może stworzyć większe możliwości.
4. **Myśl jak przestępca** – "Jak cyberprzestępca podszedłby do tematu?"

## Ważne cele:

### 1. Sensitive functionality (Funkcjonalności wrażliwe)
To części systemu, które wykonują krytyczne operacje, np. modyfikacja danych, dostęp do treści prywatnych, uruchamianie procesów systemowych.  
Jeśli atakujący uzyska dostęp do nich, może wyrządzić realne szkody.

### 2. User data (Dane użytkowników)
Informacje osobiste, np. imiona, e-maile, hasła, dane kont.  
Mogą zostać wykradzione, sprzedane lub wykorzystane do dalszych ataków (np. phishing).

### 3. Administrative features (Funkcje administracyjne)
Funkcje z wysokimi uprawnieniami, np. zarządzanie użytkownikami, zmiana konfiguracji, pełna kontrola nad aplikacją.  
Dostęp do nich daje atakującemu niemal pełną władzę nad systemem.

### 4. Further attack opportunities (Dalsze możliwości ataku)
Gdy atakujący uzyska autoryzowany dostęp, może wykorzystać inne luki w aplikacji, np. do eskalacji uprawnień, poruszania się w sieci wewnętrznej lub przejęcia kolejnych kont.
