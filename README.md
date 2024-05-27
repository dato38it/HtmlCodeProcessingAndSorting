# Обработка и сортировка Html-кода
<ul>
    <li>
        Записать в файл text.txt данные, которые нужно преобразовать
    </li>
    <li>
        Обработать файл text.txt
    </li>
    <li>
        Сохранить изменения в output.txt&nbsp;
    </li>
</ul>
<p>Task:<br>
В файле text.txt следующая информация:
<br>$ cat settings.py<br>...<br>DATABASES = {<br>&nbsp;&nbsp;&nbsp;'default': {<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;#'ENGINE': 'django.db.backends.sqlite3',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;#'NAME': BASE_DIR / 'db.sqlite3',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'ENGINE': 'django.db.backends.postgresql_psycopg2',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'PORT': '5432',<br>&nbsp;&nbsp;&nbsp;}<br>}<br>...<br>
Надо текст преобразовать в html формат и записать результат в output.txt:
<br><p>$ cat settings.py<br>...<br>DATABASES = {<br>&nbsp;&nbsp;&nbsp; 'default': {<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #'ENGINE': 'django.db.backends.sqlite3',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #'NAME': BASE_DIR / 'db.sqlite3',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 'ENGINE': 'django.db.backends.postgresql_psycopg2',<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 'PORT': '5432',<br>&nbsp;&nbsp;&nbsp; }<br>}<br>...</p><br>
Source:<br>
Чтение из файла - https://pythonworld.ru/tipy-dannyx-v-python/fajly-rabota-s-fajlami.html<br>Работа с несколькими файлами в Python - https://docs-python.ru/tutorial/chtenie-zapis-fajl/odnovremennoe-chtenie-zapis-raznye-fajly/<br>Использование встроенной функции open() - https://sky.pro/media/chtenie-fajla-postrochno-v-spisok-na-python/<br>Использование генераторов - https://sky.pro/media/chtenie-fajla-postrochno-v-spisok-na-python/?ysclid=lv9i6ky8w2363195830<br>Заменить табуляцию пробелом во всем текстовом файле python - https://translated.turbopages.org/proxy_u/en-ru.ru.8446d21d-66250fbc-1552d51e-74722d776562/https/stackoverflow.com/questions/54785152/replace-tab-with-space-in-entire-text-file-python?__ya_mt_enable_static_translations=1<br>Добавление текста в файл с помощью оператора with - https://pythonturbo.ru/kak-v-python-dobavit-tekst-v-fajl/<br></p>

