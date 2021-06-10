# rubber

## Программа *минимум*
1. запускаем скрипт с 1 аргументом *node rubber/index.js /path/to/file.wav*
2. спрашиваем elasticsearch запись с *recordingfile* == *file.wav*
3. если у elasticsearch нет записи => пропускаем файл
4. если у записи из elasticsearch есть *text* и *text_complete* == true => пропускаем файл
5. отправляем в Vosk файл и получаем его текстовое содержание.
6. обновляем запись в elasticsearch полями *text* == *данные из vosk* и *text_complete* == true

## Еще
Файлы wav можно найти с помощью find.
Длительность wav файла можно получить из soxi
