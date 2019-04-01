# [GNU Parallel](https://www.gnu.org/software/parallel/)
Zamiennik `xargs`.

Potrafi uruchamiać kilka komend w jednym ciągu (bez konieczności klepania `sh -c`), oraz równolegle wykonywać wiele poleceń.

## Demo
[![asciicast](https://asciinema.org/a/238135.svg)](https://asciinema.org/a/238135)

## Przydatne opcje
###`-j n`
uruchamia równolegle `n` poleceń

### `{}`
Wstawia pojedynczą wartość do polecenia.
```
$ seq 1 3 | parallel 'echo {}'
1
2
3
```

### `:::`
Umożliwia przekazanie stałych wartości.
```
$ parallel 'echo {}' ::: a b c
a
b
c
```

### `::::`
Umożliwia odczytanie wartości z pliku
```
$ parallel 'echo {}' :::: <(seq 1 3)
1
2
3
```
> Zapis `<(polecenie)` tworzy tymczasowy plik, zapisuje do niego wynik polecenia `polecenie` i przekazuje go jako argument.

### `{n}`
Wstawia `n`ty argument do polecenia.
```
$ parallel 'echo {1}+{2}' ::: 1 2 ::: a b
1+a
1+b
2+a
2+b
```
