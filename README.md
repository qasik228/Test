# Test

### Task 3
1) Показать какой размер этого файла и какие у него права: ls -l var/log/syslog

Написать последовательность (конвеер) команд, которая: 
4.1) считает сколько в данном файле строк: wc var/log/syslog -l

4.2) считает сколько в данном файле строк в которых встречается слово Successfully: grep Successfully var/log/syslog | wc -l;

4.3) Вывести последние три строчки в которых встречается данное слово Successfully: grep Successfully var/log/syslog | tail -3;

4.4) Вывести последнюю строчку в которой встречается Successfully , + две строчки до нее и две строчки после нее: grep -C2 Successfully var/log/syslog | tail -5;

4.5) Для последней строки , где встречается слово Successfully – вывести только первые 20 символов: grep Successfully var/log/syslog | tail -1 | cut -c -20; 	grep Successfully var/log/syslog | tail -1 | head -c 20.

### Демонстрация работы команд
(ВАЖНО: для полной демонстрации работы команд, в пунктах 4.2-4.5 команда grep используется с флагом -i)
1) ls -l var/log/syslog
[![asciicast](https://asciinema.org/a/HBHP8KXSxTqlyLrd7TfOXmagn.svg)](https://asciinema.org/a/HBHP8KXSxTqlyLrd7TfOXmagn)

4.1) wc var/log/syslog -l
[![asciicast](https://asciinema.org/a/JQ2SImeZ0AcfhigD66VK6LRE2.svg)](https://asciinema.org/a/JQ2SImeZ0AcfhigD66VK6LRE2)

4.2) grep Successfully var/log/syslog | wc -l;
[![asciicast](https://asciinema.org/a/CqLRtIQ57zTs199djYfUkEqef.svg)](https://asciinema.org/a/CqLRtIQ57zTs199djYfUkEqef)

4.3) grep Successfully var/log/syslog | tail -3;
[![asciicast](https://asciinema.org/a/cOpIPEpxoZcYfOW7HalZegH3w.svg)](https://asciinema.org/a/cOpIPEpxoZcYfOW7HalZegH3w)

4.4) grep -C2 Successfully var/log/syslog | tail -5;
[![asciicast](https://asciinema.org/a/t5n9xv3yPgGwhlQXbz8NyE6cb.svg)](https://asciinema.org/a/t5n9xv3yPgGwhlQXbz8NyE6cb)

4.5) grep Successfully var/log/syslog | tail -1 | cut -c -20; 	grep Successfully var/log/syslog | tail -1 | head -c 20.
[![asciicast](https://asciinema.org/a/Wk9fCjYmA9IuULFwKzr9Qc3wl.svg)](https://asciinema.org/a/Wk9fCjYmA9IuULFwKzr9Qc3wl)