## Szyfrowanie Symetryczne

### Pytanie:
Jeśli ktoś podsłuchuje każdy możliwy fragment danych podróżujących pomiędzy dwoma hostami, to jak umożliwić hostom wymienianie sekretów?

- **plaintext** – tekst jawny – wiadomość, np. "Siemka", albo dane, np. "Pacjent: Jan Nowak", dane przed szyfrowaniem.
- **ciphertext** – zaszyfrowany tekst jawny – Działanie algorytmu + klucza na tekst jawny. Po zaszyfrowaniu zdanie nie może mieć jakiegokolwiek sensu i to właśnie o to chodzi.
- **key** – klucz – hasło, którego używa algorytm do szyfrowania i deszyfrowania danych. Bez niego zaszyfrowany tekst ma być obliczeniowo nie do złamania.
- **Algorithm** – algorytm – dokumentacja umożliwia na zaszyfrowanie wiadomości. Każdy może znać algorytm, jednak to od klucza zależy jego oszyfrowanie. Trzymanie klucza w tajemnicy jest podstawą.

### Publicznie znany sposób szyfrowania
I to jest bardzo ważne:

**Bezpieczeństwo nie może zależeć od tajności algorytmu, tylko od tajności klucza.**

To zasada **Kerckhoffsa**.

### Drugi problem: Jak wymienić klucze pomiędzy hostami, tak żeby nikt nie podłuchał?

Aby bezpiecznie przesłać klucz, musisz mieć już bezpieczny kanał.  
Aby mieć bezpieczny kanał, musisz mieć klucz.  
Stąd mamy kryptografię asymetryczną.

---

## Szyfrowanie Asymetryczne

Zamiast jednego klucza, mamy:

- **klucz publiczny** (może go znać każdy)
- **klucz prywatny** (zna go tylko właściciel)

Najczęściej używamy:

- RSA
- Diffie-Hellman
- Elliptic Curve

### Jak to działa w praktyce?

1. Klient łączy się z serwerem.
2. Serwer wysyła klientowi swój certyfikat zawierający klucz publiczny.
3. Klient generuje losowy klucz symetryczny.
4. Szyfruje go kluczem publicznym serwera i wysyła do serwera.
5. Serwer odszyfrowuje go swoim kluczem prywatnym.
6. Od tego momentu komunikacja idzie symetrycznie, bo obie strony posiadają klucz do symetrycznego odszyfrowania wiadomości.
