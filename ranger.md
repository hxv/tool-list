# [ranger](https://ranger.github.io/)
Manager plików, po prostu.

## Demo
[![asciicast](https://asciinema.org/a/239047.svg)](https://asciinema.org/a/239047)

## Przydatne opcje
### `spacja`
Zaznacza plik

### `v`
Zaznacza wszystkie pliki w katalogu

### `:mark [pattern]`
Zaznacza wszystkie pliki w katalogu pasujące do wzorca `[pattern]`.
```
:mark \.gz$
```

### `dd`
Oznacza pliki do przeniesienia.

### `da`
Dodaje pliki do przeniesienia (w przeciwieństwie do `dd` nie czyści poprzednio zaznaczonych plików).

### `yy`
Oznacza pliki do skopiowania.

### `ya`
Dodaje pliki do skopiowania (w przeciwieństwie do `yy` nie czyści poprzednio zaznaczonych plików).

### `pp`
Przenosi/kopiuje zaznaczone pliki.

### `:bulkrename`
Masowa zmiana nazw zaznaczonych plików.

### O wiele więcej
Program ma multum opcji i możliwości:
- [znane z `vi` skróty (np. `gg`/`G`)](https://ranger.github.io/ranger.1.html#KEY-BINDINGS)
- [lista ulubionych plików/katalogów](https://ranger.github.io/ranger.1.html#BOOKMARKS)
- [obsługa skojarzeń typów plików z programami (wieloma!)](https://ranger.github.io/ranger.1.html#RIFLE)
- [możliwość konfiguracji podglądu pliku w zależności od typu](https://ranger.github.io/ranger.1.html#PREVIEWS)
- [dużo więcej](https://ranger.github.io/ranger.1.html)