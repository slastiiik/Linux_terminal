<h1 align="center">Linux_terminal</h1>

1. посмотреть где я
pwd

2. создать папку
mkdir folder1

3. зайти в папку
cd folder1

4. cоздать 3 папки
mkdir folder{1,2,3}

5. зайти в любоую папку
cd folder2

6. создать 5 файлов (3 txt, 2 json)
touch file1.txt file2.txt file3.txt file4.json file5.json

7. создать 3 папки
mkdir folder4 folder5 folder6

8. вывести список содержимого папки
ls -la

9. +открыть любой txt файл
cat file1.txt 

10. +написать туда что-нибудь, любой текст
cat >> file1.txt - idi nahui

11. +сохранить и выйти
ctr+c 

12. выйти из папки на уровень выше
cd ..

13. переместить любые 2 файла, которые вы создали, в любую другую папку
mv file1.txt file2.txt folder6

14. скопировать любые 2 файла, которые вы создали, в любую другую папку 
cp file3.txt file4.json folder5

15. найти файл по имени 
find -name "file1.txt"

16. просмотреть содержимое в реальном времени (команда grep) изучите как она работает
grep 7 file1.txt

17. вывести несколько первых строк из текстового файла
head -2

18. вывести несколько последних строк из текстового файла
tail -2

19. просмотреть содержимое длинного файла (команда less) изучите как она работает
less file1.txt

20. вывести дату и время
date

Задание *
Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

1.Вариант

#!/bin/bash

cd folder1

mkdir folder{1,2,3}

cd folder1

touch {file1.txt,file2.txt,file3.txt,file4.json,file5.json}

mkdir folder{1,2,3}

ls -la

mv file1.txt file2.txt folder3

2.Вариант

#!/bin/bash

zaiti="cd folder1"

sozdat="mkdir folder1 folder2 folder3"

faili="touch file1.txt file2.txt file3.txt file4.json file5.json"

spisok="ls -la"

peremestit="mv file1.txt file2.txt folder3"

$zaiti

$sozdat

$zaiti

$faili

$sozdat

$spisok

$peremestit
