Роль nginx / The nginx Role
=========
Роль станавливает стабильную текущую версию nginx согласно инструкции с официального сайта [nginx](https://nginx.org/ru/linux_packages.html)

The role installs the stable current version of nginx according to the instructions from the official website [nginx](https://nginx.org/ru/linux_packages.html)

Используемые переменные / Role Variables:
--------------
Переменные по умолчанию / default Variables:

    # ссылка на скачиваемый пакет nginx для ОС семейства Suse
    # link to openjdk download package
    nginx_suse_repo: "'http://nginx.org/packages/sles/$releasever_major' nginx-stable"

Внутренние переменные роли / internal role variables:

    # Полное наименование файла html, который будет раздавать nginx
    # Full name of the html file that nginx will distribute
    nginx_template_html: /var/www/html/index.html

    # Директория расположения сайта конфигурации nginx для сайта
    # Nginx configuration site location directory for the site
    nginx_template_conf: /etc/nginx/conf.d/

    # Зависимости, необходимые для установки текущей стабильной версии nginx
    # Dependencies required to install the current stable version of nginx
    nginx_suse_req: 
      - curl
      - ca-certificates
      - gpg2

Пример использования роли / Example Playbook
----------------

    - hosts: servers
      roles:
         - nginx

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
