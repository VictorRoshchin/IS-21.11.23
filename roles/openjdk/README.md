Роль openjdk / The openjdk Role
=========
Роль удаляет старую версию jdk (openjdk_to_remove) и устанавливает [новую](https://openjdk.java.net/projects/jdk/17/) по ссылке на репозиторий (openjdk_url)

This role removes the old jdk version (openjdk_to_remove) and installs [the new one](https://openjdk.java.net/projects/jdk/17/) via the repository link (openjdk_url)

Используемые переменные / Role Variables:
--------------
Переменные по умолчанию / default Variables:

    # ссылка на скачиваемый пакет openjdk
    # link to openjdk download package
    openjdk_url: https://download.java.net/<archive_name>.tar.gz

    # директория установки пакета openjdk
    # openjdk package installation directory
    openjdk_root_dir: /opt

    # наименование пакета для удаления
    # name of the package to remove
    openjdk_to_remove: java-1.8.0-openjdk

Внутренние переменные роли / internal role variables:

    # Полное наименование архива после скачивания
    # Full name of the archive after downloading
    openjdk_dest: <openjdk_root_dir>/openjdk-archive.tar.gz

    # расположение исполняемых файлов openjdk / путь, который будет добавлен в PATH
    # location of openjdk executables / path to be added to PATH
    openjdk_bin: <openjdk_root_dir>/jdk-17/bin

    # расположение скрипта, который добавляет путь к исполняемым файлам openjdk в PATH
    # location of the script that adds the path to the openjdk executables to PATH
    openjdk_env_path: /etc/profile.d/java.sh

Пример использования роли / Example Playbook
----------------

    - hosts: servers
      roles:
         - openjdk

Лицензия / License
-------

**Лицензия MIT**

    Copyright © 2023 VictorRoshchin

    Данная лицензия разрешает лицам, получившим копию данного программного обеспечения и сопутствующей документации (в дальнейшем именуемыми «Программное Обеспечение»), безвозмездно использовать Программное Обеспечение без ограничений, включая неограниченное право на использование, копирование, изменение, слияние, публикацию, распространение, сублицензирование и/или продажу копий Программного Обеспечения, а также лицам, которым предоставляется данное Программное Обеспечение, при соблюдении следующих условий:

    Указанное выше уведомление об авторском праве и данные условия должны быть включены во все копии или значимые части данного Программного Обеспечения.

    ДАННОЕ ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ ПРЕДОСТАВЛЯЕТСЯ «КАК ЕСТЬ», БЕЗ КАКИХ-ЛИБО ГАРАНТИЙ, ЯВНО ВЫРАЖЕННЫХ ИЛИ ПОДРАЗУМЕВАЕМЫХ, ВКЛЮЧАЯ ГАРАНТИИ ТОВАРНОЙ ПРИГОДНОСТИ, СООТВЕТСТВИЯ ПО ЕГО КОНКРЕТНОМУ НАЗНАЧЕНИЮ И ОТСУТСТВИЯ НАРУШЕНИЙ, НО НЕ ОГРАНИЧИВАЯСЬ ИМИ. НИ В КАКОМ СЛУЧАЕ АВТОРЫ ИЛИ ПРАВООБЛАДАТЕЛИ НЕ НЕСУТ ОТВЕТСТВЕННОСТИ ПО КАКИМ-ЛИБО ИСКАМ, ЗА УЩЕРБ ИЛИ ПО ИНЫМ ТРЕБОВАНИЯМ, В ТОМ ЧИСЛЕ, ПРИ ДЕЙСТВИИ КОНТРАКТА, ДЕЛИКТЕ ИЛИ ИНОЙ СИТУАЦИИ, ВОЗНИКШИМ ИЗ-ЗА ИСПОЛЬЗОВАНИЯ ПРОГРАММНОГО ОБЕСПЕЧЕНИЯ ИЛИ ИНЫХ ДЕЙСТВИЙ С ПРОГРАММНЫМ ОБЕСПЕЧЕНИЕМ.

**The MIT License (MIT)**

    Copyright © 2023 VictorRoshchin

    Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Информация об авторе / Author Information
------------------
Почта для связи / сontact email: v.e.roshchin@mail.ru
