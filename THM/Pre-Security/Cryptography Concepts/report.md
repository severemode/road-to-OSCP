Szyfrowanie Symetryczne

Pytanie: Jeśli ktoś podsłuchuje każdy możliwy fragment danych podrozujacyc pomiedzy dwoma hostami to jak umożliwić hostom wymienianie sekretów?



plaintext - tekst jawny - wiadomość jak: "Siemka", albo dane jak : "Pacjent: Jan Nowak", dane przed szyfrowaniem

ciphertext - zaszyfrowany tekst jawny - Działanie algorytmu + klucza na tekst jawny. Po zaszyfrowaniu zdanie nie może mieć jakiegokolwiek sensu i to wlasnie o to w tym chodzi.

key - klucz - haslo ktorego uzywa algorytm na podstawie szyfruje i deszyfruje dane. Bez niego zaszyfrowany tekst ma byc obliczeniowo nie do zlamania.

Algorithm - algorytm - dokumntacja umozliwia na zaszyfrowanie wiadomosci. Kazdy moze znac algorytm jednak to od klucza zalezy jego oszyfrowanie. Wiec trzymanie klucza sekretnie jest podstawa


Publicznie znany sposób szyfrowania.
I to jest bardzo ważne:

Bezpieczeństwo nie może zależeć od tajności algorytmu, tylko od tajności klucza.

To zasada Kerckhoffsa.

Teraz drugi problem. Jak wymienic klucze pomiedzy hostami tak żeby nikt nie podłuchał?

Aby bezpiecznie przesłac klucz, musisz miec juz bezpieczny kanal.
Aby miec bezpieczny kanal, musisz miec klucz.

Stad mamy kryptografie asymetryczna


szyfrowanie asymetryczne 

zamiast jednego klucza masz 

- klucz publiczny (moze go znac kazdy)
- klucz prywatny (zna go tylko wlasciciel)

Najczęsciej uzywamy:

-RSA
-Diffie-Hellman
-Elliptic Curve


Jak to dziala w praktyce?

1. Klient laczy sie z serwerem 
2. Serwer wysyła klientowi swój certyfikat zawierający klucz publiczny.
3. klient generuje losowy klucz symetryczny
4. szyfruje go kluczem publicznym serwera i wysyla do serwera
5. serwer odszyfrowuje go swoim kluczem prywatnym
6. od tego momentu komunikacja idzie symetrycznie bo obie strony posiadaja klucz do symetrycznego odszyfrowania wiadomosci.
