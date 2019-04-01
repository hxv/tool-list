# [jq](https://stedolan.github.io/jq/)
Narzędzie do formatowania, filtrowania i przetwarzania danych w formacie JSON.

## Demo
[![asciicast](https://asciinema.org/a/237723.svg)](https://asciinema.org/a/237723)

## Przydatne opcje
### `select(condition)`
Wybiera tylko wyniki pasujące do `condition`.
```
$ echo '[1, 2, 3, 4, 5]' | jq '.[] | select(. > 2)'
3
4
5
```

### `-r`
Zwraca stringi jako zwykłe ciągi znaków (bez `"` itd.).
```
$ echo '["a", "b", "c"]' | jq '.[]' -r
a
b
c
```

### `-c`
Zwraca kompaktowe dane, dzięki czemu każde dopasowanie znajduje się w osobnej linii. Umożliwia to m.in. łatwe łączenie poleceń.
```
$ echo -e '[[1, 2], [3, 4]]' | jq '.[]' -c | jq '.[]'
1
2
3
4
```

### `-M`
Wyłącza kolorowanie. Przydatne, jeśli chcemy przekierować wyjście do pliku.
```
$ echo '"123"' | jq . -M > output
```

### `{}'
Umożliwia tworzenie nowych obiektów/przekształcanie danych.
```
$ echo '[0,1,2]' | jq '.[] | {"key": .}' -c
{"key":0}
{"key":1}
{"key":2}
```

### O wiele więcej
Więcej przykładów znajduje się w [dokumentacji](https://stedolan.github.io/jq/manual/) - normalnie za każdym razem chcemy osiągnąć inny efekt na innych danych, więc bez przeczytania jej się nie obejdzie.