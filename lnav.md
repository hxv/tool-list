# [lnav](http://lnav.org/)
Przeglądarka logów, "zamiennik" `tail`/`less`.

## Demo
[![asciicast](https://asciinema.org/a/238360.svg)](https://asciinema.org/a/238360)

## Przydatne opcje
### `Shift+P`
Włącza zawijanie linii i automatyczne wcięcia - zwiększa czytelność logów, ale sprawia, że mniej ich mieści się na ekranie.

### `p`
Wyświetla szczegóły pierwszej widocznej na ekranie linii.

### `/`
Umożliwia wyszukiwanie, aby przejść do następnego/poprzedniego wyniku możemy użyć `n`/`N`.

### `;`
Rozpoczyna wprowadzanie zapytania SQL.

### `.schema`
Wyświetla dostępne tabele.

### `strftime('format', field)` (SQLite)
Zwraca sformatowaną datę. Możliwe wartości do wstawienia w pole `format` znajdują się w [dokumentacji](https://www.sqlite.org/lang_datefunc.html).

Przydatne do grupowania logów.

### `count(expression)`
Zlicza ilość wierszy, w których wartość `expression` jest inna niż `NULL`. Przy połączeniu z np. `CASE` można liczyć wiersze w których znajdują się konkretne wartości.
```sql
SELECT
  COUNT(CASE WHEN bar = 1 THEN 1 ELSE NULL END)
  COUNT(CASE WHEN bar = 2 THEN 1 ELSE NULL END)
  COUNT(CASE WHEN bar = 3 THEN 1 ELSE NULL END)
FROM foo
```

### `:filter-in`/`:filter-out`
Pozwala na pokazanie tylko linii pasujących do wyrażenia regularnego (lub, w przypadku `filter-out` na ich ukrycie).

### `:delete-filter`
Usuwa filtr

### O wiele więcej
Program posiada naprawdę dużo funkcji, więc warto zapoznać się z jego [dokumentacją](https://lnav.readthedocs.io/en/latest/).