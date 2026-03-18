# Wersja A

**Rozwiązania należy wysłać na adres mailowy norbert.waszkowiak@wat.edu.pl**

### Zadanie 1. Liczby dodatnie

Napisz program, który wczytuje `n` (maksymalnie 100) oraz `n` liczb całkowitych, a następnie zlicza i wypisuje ile z nich jest większych od zera.
Kod programu zapisz w pliku tekstowym `zad1.txt`.

**Przykład**

**Wejście:**
```text
6
-1 0 2 3 -5 4
```
**Wyjście:**
```text
3
```

---

### Zadanie 2. Fotowoltaika
Pan Iksiński założył panele fotowoltaiczne i przez rok monitorował wykorzystanie energii w swoim gospodarstwie domowym. Prąd wytworzony przez panele jest zużywany na bieżące potrzeby gospodarstwa domowego, a jego nadmiar jest przesyłany do zakładu energetycznego. W razie braku wystarczającej ilości energii pochodzącej z paneli (np. w godzinach nocnych lub przy pochmurnej pogodzie) energia jest pobierana z zakładu energetycznego.

W kolejnych wierszach pliku `fotowoltaika.txt` są zawarte następujące informacje, rozdzielone znakami tabulacji:
* **data** – data pomiaru
* **wsch** – godzina wschodu słońca
* **zach** – godzina zachodu słońca
* **st_zach** – stopień zachmurzenia (liczba całkowita od 0 do 8, przy czym liczba 0 oznacza brak zachmurzenia, natomiast liczba 8 – całkowite zachmurzenie)
* **produkcja** – energia wyprodukowana przez całą dobę przez panele fotowoltaiczne (w kWh)
* **oddanie** – energia oddana do zakładu energetycznego przez całą dobę (w kWh)
* **pobranie** – energia pobrana z zakładu przez gospodarstwo domowe przez całą dobę (w kWh).

**Przykład:**
```text
data	wsch	zach	st_zach	produkcja	oddanie	pobranie
2022-01-01	07:42:56	15:36:07	0	7,78	3,29	4,56
2022-01-02	07:42:47	15:37:12	4	4,47	1,23	3,99
```

Z wykorzystaniem powyższych danych oraz dostępnych narzędzi informatycznych wykonaj podane zadania. Wyniki zapisz w pliku tekstowym `wyniki2.txt`. Odpowiedź do każdego zadania poprzedź numerem tego zadania.

#### Zadanie 2.1. (0–2)
Podaj, ile energii łącznie (w kWh) zużył pan Iksiński przez cały rok 2022. Zużywana energia to suma energii pobranej z zakładu energetycznego i energii wyprodukowanej przez pana Iksińskiego pomniejszonej o ilość oddaną do zakładu energetycznego.
*Uwaga: Przez cały styczeń pan Iksiński zużył 162,68 kWh.*

#### Zadanie 2.2. (0–3)
Dla każdego dnia oblicz czas nasłonecznienia w godzinach (czyli czas od wschodu do zachodu słońca). Wynik zaokrąglij w dół do liczby całkowitej.

Utwórz zestawienie, w którym dla każdej liczby godzin nasłonecznienia podasz średnie ilości wyprodukowanej energii, oddanej energii i pobranej energii. Na podstawie wykonanego zestawienia utwórz wykres liniowy porównujący te wartości w całym roku. Pamiętaj o czytelnym opisie wykresu (tytuł, legenda, tytuły osi).

**Przykład.**
Dla fragmentu danych:
```text
data	wsch	zach	st_zach	produkcja	oddanie	pobranie
2022-01-01	07:42:56	15:36:07	0	7,78	3,29	4,56
2022-01-02	07:42:47	15:37:12	4	4,47	1,23	3,99
2022-01-03	07:42:35	15:38:20	4	6,02	4,74	2,56
2022-01-04	07:42:19	15:39:30	6	2,63	1,22	5,22
2022-01-05	07:42:00	15:40:43	2	7,99	5,68	4,22
2022-01-06	07:41:38	15:41:58	3	4,65	3,24	2,57
2022-01-07	07:41:12	15:43:16	1	7,91	2,34	2,22
2022-01-08	07:40:43	15:44:36	1	7,24	2,58	2,47
2022-01-09	07:40:11	15:45:59	1	7,96	2,74	1,95
```
w dniach od 1 do 5 stycznia nasłonecznie trwa 7 godzin (po zaokrągleniu w dół do liczby całkowitej), a od 6 do 9 stycznia – 8 godzin (również po odpowiednim zaokrągleniu). 

---

### Zadanie 3. Instalacje
W bazie danych firmy X zawarte są informacje o instalacjach pewnej aplikacji, o urządzeniach, na których ta aplikacja została zainstalowana, oraz o krajach, w których przeprowadzono instalację.

Dane zgromadzono w plikach tekstowych: `kraje.txt`, `instalacje.txt` oraz `urzadzenia.txt`. Pierwszy wiersz każdego z plików jest wierszem nagłówkowym, a dane w wierszach rozdzielone są znakami tabulacji.

Plik o nazwie `kraje.txt` zawiera informacje o krajach, w których instalowano aplikację. W każdym wierszu pliku znajdują się następujące dane:
* **kod_k** – kod kraju (napis dwuznakowy)
* **nazwa_k** – nazwa kraju (napis do 50 znaków)
* **ludnosc_k** – ludność kraju (liczba całkowita do 10 cyfr określająca liczbę ludności).

**Przykład:**
```text
kod_k	nazwa_k	ludnosc_k
AN	NETHERLANDS ANTILES	227049
CR	COSTA RICA	5003393
DZ	ALGERIA	42545964
```

Plik o nazwie `urzadzenia.txt` zawiera informacje o urządzeniach, na których może być instalowana aplikacja. W każdym wierszu pliku znajdują się następujące informacje:
* **kod_u** – unikatowy kod (liczba całkowita co najwyżej 5-cyfrowa)
* **nazwa_u** – nazwa urządzenia (napis do 80 znaków)
* **producent_u** – producent urządzenia (napis do 35 znaków)
* **typ_u** – typ urządzenia (napis: Tablet, Phone lub PC).
*Uwaga: nazwa urządzenia nie jest unikatowa – w tabeli mogą występować dwa lub więcej urządzenia o tej samej nazwie.*

**Przykład:**
```text
kod_u	nazwa_u	producent_u	typ_u
12410	PLATINUM_E5	Sky Devices	Phone
6549	Ilium L1120	Lanix	Phone
```

Plik o nazwie `instalacje.txt` zawiera informacje o instalacjach aplikacji. W każdym wierszu pliku znajdują się następujące informacje:
* **data_i** – data instalacji (w formacie dd.mm.rrrrr)
* **kod_u** – kod urządzenia, na którym była wykonana instalacja (liczba całkowita co najwyżej 5-cyfrowa)
* **kod_k** – kod kraju, w którym znajdowało się to urządzenie (napis dwuznakowy).
*Uwaga: kod_u nie oznacza pojedynczego egzemplarza urządzenia, a tylko jego rodzaj – to znaczy na urządzeniach o tym samym kodzie może być wykonanych wiele instalacji.*

**Przykład:**
```text
data_i	kod_k	kod_u
01.03.2019	AM	145
01.03.2019	AR	804
01.03.2019	AT	12632
```

Z wykorzystaniem danych zawartych w podanych plikach oraz dostępnych narzędzi informatycznych, podaj odpowiedzi do zadań 3.1.–3.2. Odpowiedzi zapisz w pliku `wyniki3.txt`, a każdą z nich poprzedź numerem odpowiedniego zadania.

#### Zadanie 3.1. (0–2)
Dla każdego typu urządzenia podaj liczbę instalacji aplikacji na tym typie urządzenia.

#### Zadanie 3.2. (0–3)
Podaj nazwy pięciu krajów, w których przeprowadzono najwięcej instalacji w przeliczeniu na 1 000 000 mieszkańców, oraz podaj liczby tych instalacji.
Dla każdego z tych pięciu krajów podaj liczbę instalacji na 1 000 000 mieszkańców z dokładnością do dwóch miejsc po przecinku.
*Uwaga: pomiń kraje, w których jest mniej niż milion mieszkańców.*
