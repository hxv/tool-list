# [cURL](https://curl.haxx.se/)
Klient HTTP i nie tylko.

## Demo
[![asciicast](https://asciinema.org/a/237805.svg)](https://asciinema.org/a/237805)

## Przydatne opcje
### Protokół `telnet://`
Umożliwia bezpośrednie połączenie z wybranym adresem.  
Przydatne, jeśli chcemy ręcznie wprowadzić przesłane dane, lub w sprawdzić połączenie bez wysyłania zapytania HTTP (w połączeniu z opcjami `-i` i `-vvv` wyświetli status połączenia i ew. problemy).

### `-k` / `--insecure`
Wyłącza sprawdzanie poprawności certyfikatów SSL.

### `-X <metoda>`
Wysyła żądanie HTTP wybraną metodą (POST/PUT itd.).

### `-H <nagłówek>`
Dodaje nagłówek do żądania HTTP.

### `-d <dane>`
Dodaje dane do żądania HTTP.
