# Wersja B

**Rozwiązania należy wysłać na adres mailowy norbert.waszkowiak@wat.edu.pl**

### Zadanie 1. Konwersja temperatur

Napisz program, który przelicza temperaturę ze stopni Celsjusza na stopnie Fahrenheita. Program powinien wczytać jedną liczbę (temperaturę w stopniach Celsjusza), a następnie obliczyć odpowiednią wartość w stopniach Fahrenheita i wypisać wynik.
Kod programu zapisz w pliku tekstowym `zad1.txt`.

**Wzór przeliczenia:** `F = C * 9/5 + 32`

**Przykład:**

**Wejście:**
```text
0
```
**Wyjście:**
```text
32.0
```

---

### Zadanie 2. Energia odnawialna
W kolejnych wierszach pliku `energia.txt` znajdują się dane o produkcji energii ze źródeł odnawialnych (wiatrowych i fotowoltaicznych). Każdy wiersz zawiera oddzielone znakami tabulacji informacje o dacie, o godzinie oraz o liczbie megawatogodzin (MWh) wyprodukowanych przez źródła wiatrowe, a także liczbie megawatogodzin wyprodukowanych przez źródła fotowoltaiczne w kwietniu 2024. Dane są podane chronologicznie i nie zawierają luk (są podane dla każdego dnia i dla każdej godziny).

**Fragment pliku:**
```text
DataGodzinaZrodla_wiatroweZrodla_fotowoltaiczne
2024-04-0113130,2630,000
2024-04-0122765,5880,000
2024-04-0132555,4380,000
2024-04-0142675,2380,000
2024-04-0152681,1750,000
2024-04-0162367,3250,213
2024-04-0172525,225117,075
2024-04-0182360,9881162,075
2024-04-0191940,8382680,513
```

Z wykorzystaniem opisanych danych oraz dostępnych narzędzi informatycznych wykonaj następujące zadania. Wyniki zapisz w pliku tekstowym `wyniki2.txt`. Odpowiedź do każdego zadania poprzedź numerem zadania.

#### Zadanie 2.1. (0–2)
Podaj dzień, w którym łącznie wytworzono najwięcej MWh energii ze źródeł wiatrowych, oraz dzień, w którym łącznie wytworzono najwięcej MWh energii ze źródeł fotowoltaicznych w badanym okresie. W obu podanych kategoriach jest tylko jeden taki dzień.

#### Zadanie 2.2. (0–3)
Podaj dla każdej godziny w dobie (od 1 do 24) średnią liczbę wyprodukowanych MWh energii ze źródeł fotowoltaicznych w tej godzinie w kwietniu. Podaj wyniki z dokładnością do dwóch miejsc po przecinku. Dla tego zestawienia wykonaj wykres kolumnowy. Wstaw tytuł wykresu i opisz osie.

---

### Zadanie 3. Szczepienia
W pewnym centrum medycznym odbywają się szczepienia. Lekarz przepisuje pacjentowi odpowiednią szczepionkę, a każda szczepionka ma rekomendowaną liczbę dawek. Pacjent zostaje uznany za zaszczepionego, jeśli przyjmie wszystkie dawki rekomendowane dla danej szczepionki.

Dane dotyczące szczepień od 2 stycznia 2023 do 7 maja 2024 są zapisane w dwóch plikach: `szczepionki.txt` oraz `wizyty.txt`. Pierwszy wiersz w każdym pliku jest wierszem nagłówkowym i zawiera nazwy odpowiednich pól. Dane w wierszach rozdzielone są znakiem tabulacji.

Plik o nazwie `szczepionki.txt` zawiera informacje o szczepionkach. W każdym wierszu znajduje się:
* **kod_szczepionki** – tekst do 10 znaków, określający jednoznacznie szczepionkę
* **liczba_dawek** – liczba rekomendowanych dawek, liczba całkowita większa od 0 i mniejsza od 10

**Przykład:**
```text
kod_szczepionkiliczba_dawek
sz1_3d3
sz2_1d1
```

Plik o nazwie `wizyty.txt` zawiera informacje o podanej pacjentowi dawce szczepionki. W każdym wierszu znajduje się:
* **pesel** – numer PESEL pacjenta przyjmującego daną dawkę szczepienia, składający się z 11 znaków
* **kod_szczepionki** – kod podanej szczepionki
* **data_szczepienia** – data szczepienia w formacie rrrr-mm-dd
* **numer_dawki** – liczba całkowita mniejsza od 10 określająca, która dawka szczepionki została podana.

**Przykład:**
```text
Peselkod_szczepionkidata_szczepienianumer_dawki
79051863861sz16_1d2023-01-021
84100517145sz13_5d2023-01-021
```

Z wykorzystaniem danych zawartych w podanych plikach oraz dostępnych narzędzi informatycznych podaj odpowiedzi do zadań 3.1.–3.2. Odpowiedzi zapisz w pliku `wyniki3.txt`, a każdą z nich poprzedź numerem odpowiedniego zadania.

#### Zadanie 3.1. (0–2)
Dla każdej szczepionki podaj, ile łącznie jej dawek zostało podanych pacjentom. Jako wynik podaj listę zawierającą kod szczepionki i liczbę dawek. Lista powinna być posortowana nierosnąco według liczby dawek.

#### Zadanie 3.2. (0–3)
Podaj, ilu różnych pacjentów przyjęło przynajmniej jedną dawkę szczepionki o kodzie `sz12_3d`. Podaj, ile wśród nich było kobiet (płeć określa przedostatnia cyfra numeru PESEL, cyfra parzysta oznacza płeć żeńską).
