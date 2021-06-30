### Домашнее задание №1

2. **Создать папку -** `mkdir foldername`
3. **Зайти в папку -** `cd foldername`
4. **Создать три папки -** `mkdir first_folder second_folder third_folder`
5. **Зайти в любую папку -** `cd foldername`
6. **Создать 5 файлов -** `touch 1.txt 2.txt 3.txt 1.json 2.json`
7. **Создать три папки -** `mkdir first_folder second_folder third_folder`
8. **Вывести список содержимого папки -** `ls`
9. **Открыть любой txt файл -** `cat 1.txt`
10. **Написать туда что-нибудь -** `vim 1.txt` - клавиша i
11. **Сохранить и выйти - клавиша Esc, выходим в командный режим вводим
    ":" далее "qw" для сохранения и выхода.
12. **Выйти из папки на уровень выше -** `cd ..`
13. **Переместить любые два файла которые создали, в любую другую папку -** `mv 1.json 1.txt ./qa_ksendzov_dz_1cp` 
14. **Cкопировать любые 2 файла, которые вы создали, в любую другую папку -** `cp 2.json 2.txt ~/qa_ksendzov_dz_1/`
15. **Найти файл по имени -** `find / -name "1.txt"`
16. **Просмотреть содержимое в реальном времени (команда grep) изучите как она работает -** `grep -roP ".{0,8}russia.{0,74}" region.json`
оторбразит на экране строку соответствующую ключу russia и ограничет вывод 8 символами до и 74 после. Файл сгенерирован из запроса к сайту:
https://api.quarantine.country/api/v1/regions
17. **Вывести несколько первых строк из текстового файла -** `head -n5 README.md`
18. **Вывести несколько последних строк из текстового файла -** `tail -n5 README.md`
19. **Просмотреть содержимое длинного файла (команда less) изучите как она работает -** `less region.json`
20. **Вывести дату и время -** `date`

**Отправить запрос на сервер:** `curl -o region.json https://api.quarantine.country/api/v1/regions`
запишем ответ запроса в файл region.json

**Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13**

Командой `chmod ugo+x script` делаем файл исполняемым
Командой `bash script`
Текст скрипта:
```~#!/bin/bash
echo "Скрипт"
mkdir main_folder
cd main_folder
mkdir first_folder second_folder third_folder
cd first_folder
touch 1.txt 2.txt 3.txt 1.json 2.json
mkdir four_folder five_folder six_folder
mv 1.json 1.txt five_folder```





