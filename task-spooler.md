# [task-spooler](http://vicerveza.homeunix.net/~viric/soft/ts/)
Kolejkowanie zadań.

Zadania uruchamiane są kolejno w tle (także po zakończeniu sesji).  
Każde zadanie posiada zapisany wynik, który możemy sprawdzić w dogodnym momencie. Możliwe jest również uzależnienie wykonania zadania od poprawnego zakończenia poprzedniego, wskazanego przez nas, polecenia w kolejce.

Przydatne, jeśli potrzebujemy uruchomić kolejko kilka długo trwających komend, których nie chcemy uruchamiać jednocześnie.

## Demo
[![asciicast](https://asciinema.org/a/241002.svg)](https://asciinema.org/a/241002)

## Najważniejsze opcje
### `-c [n]`
Pokazuje wynik działania polecenia o numerze `n`.

### `-k [n]`
Zabija polecenie o numerze `n`.

### `-C`
Czyści zakończone zadania.
