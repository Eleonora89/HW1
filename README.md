1) Посмотреть где я - 
Pwd

2) Создать папку – 
mkdir homework_1

3) Зайти в папку – 
cd homework_1

4) Создать 3 папки –
 mkdir home_1 home_2 home_3

5) Зайти в любую папку – 
cd home_1 

6) Создать 5 файлов (3 txt, 2 json) – 
touch text_1.txt text_2.txt text_3.txt text_4.json text_5.json

or

touch q{0..2}.txt q{3..4}.json

7) Создать 3 папки – 
mkdir a_1 b_1 c_1

mkdir q{0..4}

8) Вывести список содержимого папки- 
 ls -la

9) + Открыть любой txt файл – 
vim text_1.txt

10) + написать туда что-нибудь, любой текст- 
 I, { “name”: “Eleonora”  }

11) + сохранить и выйти – 
 esc  :wq enter

12) Выйти из папки на уровень выше – 
cd ..

13) переместить любые 2 файла, которые вы создали, в любую другую папку – 
         1 вариант находимся в папке, где лежат эти файлы -  
 mv text_1.txt text_2.txt ../home_2
         2 вариант в находимся в папке, где лежат эти файлы -  
mv text_4.json text_5.json /c/Users/Элеонора/Desktop/homework_1/home_2 (абсолютный путь к папке)
         3 вариант в находимся в папке, где лежат эти файлы
mv text_3.txt text_4.json .. две точки перенесут в папку повыше(в ту папку где находится сама папка из которой достаешь)
         4 вариант находимся в общей папке и там есть 2 файла q1.txt q2.txt перенесем их в папку2
mv q1.txt  q2.txt ./папка2
         5 вариант: находясь в общей папке:
mv папка1/файл1.расширение  папка1/файл2.расширение папка2

14) скопировать любые 2 файла, которые вы создали, в любую другую папку – 
           cp text_4.json text_5.json /c/Users/Элеонора/Desktop/homework_1/home_1
второй вариант внутри главной папки перемещение из папки в папку из home_1 в home_2
cp text_{4..5}.* /c/Users/Элеонора/Desktop/homework_1/home_1

15) Найти файл по имени –
 find  -iname "text_1.txt"
можно и без точки

16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.
tail -f text_2.txt

17) вывести несколько первых строк из текстового файла
grep -m2 "" text_2.txt , где m2 две строки
head


18) вывести несколько последних строк из текстового файла
tail -2 text_2.txt, где 2 это последние 2 строчки файла
19) просмотреть содержимое длинного файла (команда less) изучите как она работает.
less text_2.txt

20) вывести дату и время
date


***
Отправить http запрос на сервер.  http://162.55.220.72:5005/object_info_3?name=Vadim&age=32&salary=1000

Запрос: curl "http://162.55.220.72:5005/object_info_3?name=Vadim&age=32&salary=1000"

***
Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
\#!/bin/bash
mkdir qw1
cd qw1
mkdir qw2 qw3 qw4
cd qw2
touch text_1.txt text_2.txt text_3.txt text_4.json text_5.json
mkdir a_1 b_1 c_1
ls -la
mv text_1.txt text_2.txt ../qw3



