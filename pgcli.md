# [pgcli](https://www.pgcli.com/)
Zamiennik `psql`.

Interaktywna konsola PostgreSQL.

## Demo
[![asciicast](https://asciinema.org/a/237719.svg)](https://asciinema.org/a/237719)

## Przydatne opcje

### Plik `~/.config/pgcli/config`
Plik `~/.config/pgcli/config` zawiera domyślną konfigurację.

#### `auto_expand = True`
Automatycznie decyduje, jak wyświetlać wyniki. Jeśli szerokość terminala na to pozwala, wyświetli pojedynczy wiersz w jednej linii. Jeśli jest za mało miejsca, to każda kolumna z danego wiersza będzie prezentowana w osobnej linijce.

### `query; \watch n`
Uruchamia zapytanie `query` co `n` sekund.

`Ctrl+C` umożliwia na przerwanie zapytania.
```
postgres> select 1; \watch 2
+------------+
| ?column?   |
|------------|
| 1          |
+------------+
SELECT 1
Time: 0.024s
Waiting for 2 seconds before repeating
+------------+
| ?column?   |
|------------|
| 1          |
+------------+
SELECT 1
Time: 0.028s
Waiting for 2 seconds before repeating
^Cpostgres>
```

### `\#`
Odświeża informacje o strukturze bazy. Przydatne, jeśli w trakcie połączenia zmieni się schema - po odświeżeniu podpowiedzi będą uaktualnione.