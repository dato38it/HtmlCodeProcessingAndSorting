<p>
    Цель:<br>
    # Преобразовать текст в html код формат.<br>
    # Изменить тэги по по запросу руководства.<br>
    Skills:<br>
    # Обработка и сортирока Html-кода.<br>
    # Парсинг сайта.<br>
    <strong>Task:</strong><br>
    В файле input.txt надо обычный текст преобразовать в html код формат, добавив только необходимые тэги, и записать результат в output.html.<br>
    # Обработка и сортирока Html-кода.<br>
    <strong>Decision:</strong><br>
    root@kvmubuntu:~# vim py.py<br>
    root@kvmubuntu:~# cat py.py<br>
    #tag - теги html<br>
    #file - переменная файла<br>
    #fileread - считывание файла<br>
    #replacetags - замена тегов<br>
    #addtags - добавление тега p в файле<br>
    #tags=["&lt;p&gt;","&lt;/p&gt;","&lt;br&gt;","&nbsp;&nbsp;&nbsp;"]<br>
    tags=["&lt;", "&gt;", "&lt;br&gt;", "&nbsp;&nbsp;", "&lt;strong&gt;<strong>Task:</strong>&lt;/strong&gt;", "&lt;strong&gt;<strong>Decision:</strong>&lt;/strong&gt;", "&lt;strong&gt;<strong>Source:</strong>&lt;/strong&gt;"]<br>
    #print(tags[2])<br>
    with open("text.txt") as file:<br>
    &nbsp;&nbsp;fileread = file.read()<br>
    &nbsp;&nbsp;#print(fileread)<br>
    replacetags=fileread.replace("&lt;", tags[0]).replace("&gt;",tags[1]).replace("\n", tags[2]).replace("&nbsp;&nbsp;", tags[3]).replace("<strong>Task:</strong>", tags[4]).replace("<strong>Decision:</strong>", tags[5]).replace("<strong>Source:</strong>", tags[6])<br>
    #print(replacetags)<br>
    addtags = "&lt;p&gt;"+replacetags+"&lt;/p&gt;"<br>
    with open("output.txt", "w") as file:<br>
    &nbsp;&nbsp;file.write(addtags+"\n")<br>
    <strong>Source:</strong><br>
    # <a href="https://pythonworld.ru/tipy-dannyx-v-python/fajly-rabota-s-fajlami.html">https://pythonworld.ru/tipy-dannyx-v-python/fajly-rabota-s-fajlami.html</a> - Чтение из файла.<br>
    # <a href="https://docs-python.ru/tutorial/chtenie-zapis-fajl/odnovremennoe-chtenie-zapis-raznye-fajly/">https://docs-python.ru/tutorial/chtenie-zapis-fajl/odnovremennoe-chtenie-zapis-raznye-fajly/</a> - Работа с несколькими файлами в Python.<br>
    # <a href="https://sky.pro/media/chtenie-fajla-postrochno-v-spisok-na-python/">https://sky.pro/media/chtenie-fajla-postrochno-v-spisok-na-python/</a> - Использование встроенной функции open().<br>
    # <a href="https://sky.pro/media/chtenie-fajla-postrochno-v-spisok-na-python/?ysclid=lv9i6ky8w2363195830">https://sky.pro/media/chtenie-fajla-postrochno-v-spisok-na-python/?ysclid=lv9i6ky8w2363195830</a> - Использование генераторов.<br>
    # <a href="https://translated.turbopages.org/proxy_u/en-ru.ru.8446d21d-66250fbc-1552d51e-74722d776562/https/stackoverflow.com/questions/54785152/replace-tab-with-space-in-entire-text-file-python?__ya_mt_enable_static_translations=1">https://translated.turbopages.org/proxy_u/en-ru.ru.8446d21d-66250fbc-1552d51e-74722d776562/https/stackoverflow.com/questions/54785152/replace-tab-with-space-in-entire-text-file-python?__ya_mt_enable_static_translations=1</a> - Заменить табуляцию пробелом во всем текстовом файле python.<br>
    # <a href="https://pythonturbo.ru/kak-v-python-dobavit-tekst-v-fajl/">https://pythonturbo.ru/kak-v-python-dobavit-tekst-v-fajl/</a> - Добавление текста в файл с помощью оператора with<br>
    <strong>Task:</strong><br>
    На странице https://tdomain.ru/sveden/education под поле "Образовательная программа, направленность, профиль, шифр и наименование научной специальности" в таблице "Образование" (информация по образовательным программам) необходимо добавить тег itemprop="eduProf". В данной таблице тег &lt;tr itemprop="eduOp"&gt;, который нужно заменить на &lt;tr itemprop="eduOprog"&gt;.<br>
    # Парсинг сайта.<br>
    <strong>Decision:</strong><br>
    БУДЕТ КОД. ИНФОРМАЦИЯ БУДЕТ ДОПОЛНЯТЬСЯ. ШАГИ ВЫПОЛНЕНИЯ:<br>
    1. Прорамма будет апрашивать страницу для парсинга.<br>
    2. Парсинг страницы сайта по тегам<br>
    3. Поиск тега который нужно аменить<br>
    4. амена тега<br>
    5. Публикация именения на сайт
</p>