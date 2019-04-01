# [pcregrep](https://www.pcre.org/original/doc/html/pcregrep.html)
Odpowiednik polecenia `grep` ze wsparciem dla PCRE (wyrażenia regularne perla).

## Demo
[![asciicast](https://asciinema.org/a/237800.svg)](https://asciinema.org/a/237800)

## Przydatne opcje
### `-oN`
Zwraca tylko dopasowania w grupie `N`.

```
$ echo '123' | pcregrep -o1 '\d(\d)\d'
2
```

### `--line-buffered`
Włącza buforowanie tylko pojedynczej linii (w połączeniu z `tail -f` wyświetla pasujące linie bez opóźnień).
```
$ tail -f log.file | pcregrep --line-buffered --buffer-size=1M '127\.0\.0\.1'
```
> Jeśli w pliku znajdują się długie linie trzeba dodać opcję `--buffer-size=1M` - zwiększa ona maksymalny rozmiar bufora dla linii.