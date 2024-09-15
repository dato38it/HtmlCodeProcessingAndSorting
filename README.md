# обработка и сортировка данных на сайтах

<p># Обработка и сортирока Html-кода.<br>
# Парсинг сайта.</p>
<p><strong>Task:</strong><br>
Обработка и сортирока Html-кода. В файле text.txt следующая информация:
<br>$ cat settings.py<br>...<br>DATABASES = {<br>&nbsp;&nbsp;&nbsp;'default': {<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;#'ENGINE': 'django.db.backends.sqlite3',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;#'NAME': BASE_DIR / 'db.sqlite3',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'ENGINE': 'django.db.backends.postgresql_psycopg2',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'PORT': '5432',<br>&nbsp;&nbsp;&nbsp;}<br>}<br>...<br>
Надо текст преобразовать в html формат и записать результат в output.txt:
<br><p>$ cat settings.py<br>...<br>DATABASES = {<br>&nbsp;&nbsp;&nbsp; 'default': {<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #'ENGINE': 'django.db.backends.sqlite3',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #'NAME': BASE_DIR / 'db.sqlite3',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 'ENGINE': 'django.db.backends.postgresql_psycopg2',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 'PORT': '5432',<br>&nbsp;&nbsp;&nbsp; }<br>}<br>...</p><br>
Source:<br>
# https://pythonworld.ru/tipy-dannyx-v-python/fajly-rabota-s-fajlami.html - Чтение из файла.<br>
# https://docs-python.ru/tutorial/chtenie-zapis-fajl/odnovremennoe-chtenie-zapis-raznye-fajly/ - Работа с несколькими файлами в Python.<br>
# https://sky.pro/media/chtenie-fajla-postrochno-v-spisok-na-python/ - Использование встроенной функции open().<br>
# https://sky.pro/media/chtenie-fajla-postrochno-v-spisok-na-python/?ysclid=lv9i6ky8w2363195830 - Использование генераторов.<br>
# https://translated.turbopages.org/proxy_u/en-ru.ru.8446d21d-66250fbc-1552d51e-74722d776562/https/stackoverflow.com/questions/54785152/replace-tab-with-space-in-entire-text-file-python?__ya_mt_enable_static_translations=1 - Заменить табуляцию пробелом во всем текстовом файле python.<br>
# https://pythonturbo.ru/kak-v-python-dobavit-tekst-v-fajl/ - Добавление текста в файл с помощью оператора with<br>
<strong>Task:</strong><br>
Парсинг сайта. Проверить все страницы сайта на отсутствие pdf файлов больше 15 Мб.<br>
<strong>Decision:</strong><br>
$ wget https://tsite.ru/sveden/document<br>
--2018-11-01 20:12:20-- https://tsite.ru/sveden/document<br>
Распознаётся tsite.ru (tsite.ru)… IpAddr<br>
Подключение к tsite.ru (tsite.ru)|IpAddr|:443... соединение установлено.<br>
ОШИБКА: Нет доверия сертификату для «tsite.ru».<br>
ОШИБКА: Неизвестный издатель сертификата «tsite.ru».<br>
$ wget --no-check-certificate -r -l 1 -A pdf https://tsite.ru/sveden/document<br>
$ vim FileWeight.sh<br>
$ chmod +x FileWeight.sh<br>
$ cat FileWeight.sh<br>
#!/bin/bash<br>
echo -n "Enter a link to the site: "<br>
read linksite<br>
user=$(whoami)<br>
echo -n "Come up with a name for the directory where the files will be written: "<br>
read linkfiles<br>
if [ -d /home/$user/$linkfiles ]; then<br>
rm -rf /home/$user/$linkfiles<br>
echo "/home/$user/$filename delete"<br>
else<br>
mkdir /home/$user/$linkfiles<br>
cd /home/$user/$linkfiles<br>
echo "/home/$user/$linkfiles create"<br>
fi<br>
wget --no-check-certificate -r -l 1 -A pdf $linksite<br>
find /home/$user/$linkfiles -size +15M &gt; output<br>
$ ./FileWeight.sh<br>
Enter a link to the site: https://tsite.ru/sveden/document<br>
Come up with a name for the directory where the files will be written: tdir<br>
/home/tUser/tdir create<br>
...<br>
$ cat /home/tUser/tdir/output<br>
/home/tUser/tdir/tsite.ru/Media/irk/Документы института/2018/tDoc1.pdf<br>
$ ls -l /home/tUser/tdir/tsite.ru/Media/irk/Документы\ института/2018/tDoc1.pdf&nbsp;<br>
-rw-r--r--. 1 tUser tUser 20055320 июн 30 2018 '/home/tUser/tdir/tsite.ru/Media/irk/Документы института/2018/tDoc1.pdf'<br>
<strong>Task:</strong><br>
Отсортировать html-код страницы по атрибутам &lt;tr&gt;&lt;td&gt;<br>
<strong>Decision:</strong><br>
<strong>Task:</strong><br>
Поменять/добавить тег на странице с таблицей,в некоторых строках тег отсутствует<br>
<strong>Decision:</strong><br>
<strong>Source:</strong><br>
# https://stackoverflow.com/questions/4846007/check-if-directory-exists-and-delete-in-one-command-unix<br>
</p>