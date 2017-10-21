[Вопросы для собеседования на Java Junior](README.md)

# Основы Web
+ [Что такое _WWW_?](#Что-такое-www)
+ [Что такое _W3C_?](#Что-такое-w3c)
+ [Какие существуют уровни модели _OSI_?](#Какие-существуют-уровни-модели-osi)
+ [Что такое _TCP/IP_?](#Что-такое-tcpip)
+ [Что такое _UDP_?](#Что-такое-udp)
+ [Чем отличаются _TCP_ и _UDP_?](#Чем-отличаются-tcp-и-udp)
+ [Что такое протокол передачи данных? Какие протоколы вы знаете?](#Что-такое-протокол-передачи-данных-Какие-протоколы-вы-знаете)
+ [Что такое _HTTP_ и _HTTPS_? Чем они отличаются?](#Что-такое-http-и-https-Чем-они-отличаются)
+ [Что такое _FTP_?](#Что-такое-ftp)
+ [Чем отличаются методы _GET_ и _POST_?](#Чем-отличаются-методы-get-и-post)
+ [Что такое _MIME тип_?](#Что-такое-mime-тип)
+ [Что такое _Web server_?](#Что-такое-web-server)
+ [Что такое _Web application_?](#Что-такое-web-application)
+ [Что такое _Application server_?](#Что-такое-application-server)
+ [Чем отличаются _Web server_ и _Application server_?](#Чем-отличаются-web-server-и-application-server)
+ [Что такое _AJAX_? Как принципиально устроена эта технология?](#Что-такое-ajax-Как-принципиально-устроена-эта-технология)
+ [Что такое _WebSocket_?](#Что-такое-websocket)
+ [Что такое _JSON_?](#Что-такое-json)
+ [Что такое _JSON схема_?](#Что-такое-json-схема)
+ [Что такое _cookies_?](#Что-такое-cookies)
+ [Что такое _«сессия»_?](#Что-такое-сессия)
+ [Что такое _«авторизация»_ и _«аутентификация»_? Чем они отличаются?](#Что-такое-авторизация-и-аутентификация-Чем-они-отличаются)

## Что такое _WWW_?
__WWW, World Wide Web (Всемирная паутина)__ — распределённая система, предоставляющая доступ к связанным между собой документам, расположенным на различных компьютерах, подключённых к Интернету. Для обозначения этого термина также используют слово _web_.

[к оглавлению](#Основы-web)

## Что такое _W3C_?
__W3C, World Wide Web Consortium (Консорциум Всемирной паутины)__ — организация, разрабатывающая и внедряющая технологические стандарты для WWW. 

W3C разрабатывает для Интернета единые принципы и стандарты, называемые _«рекомендациями» (W3C Recommendations)_, которые затем внедряются производителями программ и оборудования. Таким образом достигается совместимость между программными продуктами и аппаратурой различных компаний.

[к оглавлению](#Основы-web)

## Какие существуют уровни модели _OSI_?
| # |                  Уровень (layer)                 |               Тип данных (PDU)            |                          Функции                         |          Примеры           |
|--:|--------------------------------------------------|:-----------------------------------------:|----------------------------------------------------------|:--------------------------:|
| 7 | Прикладной (application)                         |                      -                    | Доступ к сетевым службам                                 | HTTP, FTP                  |
| 6 | Представительский (представления) (presentation) |                      -                    | Представление и шифрование данных                        | ASCII, JPEG                |
| 5 | Сеансовый (session)                              |                      -                    | Управление сеансом связи                                 | RPC, PAP                   |
| 4 | Транспортный (transport)                         | Сегменты(segment) / Дейтаграммы(datagram) | Прямая связь между конечными пунктами и надежность       | TCP, UDP                   |
| 3 | Сетевой (network)                                |              Пакеты (packet)              | Определение маршрута и логическая адресация              | IP, AppleTalk              |
| 2 | Канальный (data link)                            |         Биты (bit) / Кадры (frame)        | Физическая адресация                                     | Ethernet, IEEE 802.2, L2TP |
| 1 | Физический (physical)                            |                  Биты (bit)               | Работа со средой передачи, сигналами и двоичными данными | USB, витая пара            |

[к оглавлению](#Основы-web)

## Что такое _TCP/IP_?
__TCP/IP__ - это два основных сетевых протокола Internet. Часто это название используют и для обозначения сетей, работающих на их основе.

__IP (Internet Protocol)__ - маршрутизируемый протокол, отвечающий за IP-адресацию, маршрутизацию, фрагментацию и восстановление пакетов. В его задачу входит продвижение пакета между сетями – от одного маршрутизатора до другого и тех пор, пока пакет не попадет в сеть назначения. В отличие от протоколов прикладного и транспортного уровней, протокол IP разворачивается не только на хостах, но и на всех шлюзах (маршрутизаторах). Этот протокол работает без установления соединения и без гарантированной доставки.

В настоящее время используются следующие две версии протокола IP:

+ _IPv6_ — IP-адрес имеет разрядность 128 бит и записывается в виде восьми 16-битных полей, с использованием шестнадцатеричной системы счисления и с возможностью сокращения двух и более последовательных нулевых полей до `::`, например: `2001:db8:42::1337:cafe`
+ _IPv4_ — IP-адрес имеет разрядность 32 бита и записывается в виде четырех десятичных чисел в диапазоне 0 … 255 через точку, например: `192.0.2.34`.

__TCP (Transfer Control Protocol)__ - протокол, обеспечивающий надежную, требующую логического соединения связь между двумя компьютерами. Отвечает за установление соединения, упорядочивание посылаемых пакетов и восстановление пакетов, потерянных в процессе передачи.

Стек протоколов _TCP/IP_ включает в себя четыре уровня:

1. _канальный уровень (link layer)_ - например Ethernet, IEEE 802.11 Wireless Ethernet, физическая среда и принципы кодирования информации
2. _сетевой уровень (Internet layer)_ - например IP
3. _транспортный уровень (transport layer)_ - например TCP, UDP
4. _прикладной уровень (application layer)_ - например HTTP, FTP, DNS

TCP-соединение двух узлов начинается с _handshake (рукопожатия)_:

+ Узел _A_ посылает узлу _B_ специальный пакет `SYN` — приглашение к соединению
+ _B_ отвечает пакетом `SYN-ACK` — согласием об установлении соединения
+ _A_ посылает пакет `ACK` — подтверждение, что согласие получено

После этого _TCP соединение_ считается установленным и приложения, работающие в этих узлах, могут посылать друг другу пакеты с данными.

В заголовке _TCP/IP_ пакета указывается:

+ IP-адрес отправителя
+ IP-адрес получателя
+ Номер порта

[к оглавлению](#Основы-web)

## Что такое _UDP_?
__UDP, User Datagram Protocol (Протокол пользовательских датаграмм)__ — протокол, который обеспечивает доставку без требований соединения с удаленным модулем UDP и обязательного подтверждения получения. 

К заголовку IP-пакета UDP добавляет всего четыре поля по 2 байта каждое:

1. _поле порта источника (source port)_
2. _поле порта пункта назначения (destination port)_
3. _поле длины (length)_
4. _поле контрольной суммы (checksum)_

Поля «порт источника» и «контрольная сумма» не являются обязательными для использования в IPv4. В IPv6 необязательно только поле «порт отправителя».

UDP используется _DNS_, _SNMP_, _DHCP_ и другими приложениями.

[к оглавлению](#Основы-web)

## Чем отличаются _TCP_ и _UDP_?
__TCP__ — ориентированный на соединение протокол, что означает необходимость «рукопожатия» для установки соединения между двумя хостами. Как только соединение установлено, пользователи могут отправлять данные в обоих направлениях.

+ _Надёжность_ — TCP управляет подтверждением, повторной передачей и тайм-аутом сообщений. Производятся многочисленные попытки доставить сообщение. Если оно потеряется на пути, сервер вновь запросит потерянную часть. В TCP нет ни пропавших данных, ни (в случае многочисленных тайм-аутов) разорванных соединений.
+ _Упорядоченность_ — если два сообщения последовательно отправлены, первое сообщение достигнет приложения-получателя первым. Если участки данных приходят в неверном порядке, TCP отправляет неупорядоченные данные в буфер до тех пор, пока все данные не могут быть упорядочены и переданы приложению.
+ _Тяжеловесность_ — TCP необходимо три пакета для установки соединения перед тем, как отправить данные. TCP следит за надёжностью и перегрузками.
+ _Потоковость_ — данные читаются как поток байтов, не передается никаких особых обозначений для границ сообщения или сегментов.

__UDP__ — более простой, основанный на сообщениях протокол без установления соединения. Протоколы такого типа не устанавливают выделенного соединения между двумя хостами. Связь достигается путём передачи информации в одном направлении от источника к получателю без проверки готовности или состояния получателя.

+ _Ненадёжность_ — когда сообщение посылается, неизвестно, достигнет ли оно своего назначения — оно может потеряться по пути. Нет таких понятий как подтверждение, повторная передача, тайм-аут.
+ _Неупорядоченность_ — если два сообщения отправлены одному получателю, то порядок их достижения цели не может быть предугадан.
+ _Легковесность_ — никакого упорядочивания сообщений, никакого отслеживания соединений и т. д. Это лишь транспортный уровень.
+ _Датаграммы_ — пакеты посылаются по отдельности и проверяются на целостность только если они прибыли. Пакеты имеют определенные границы, которые соблюдаются после получения, то есть операция чтения на получателе выдаст сообщение таким, каким оно было изначально послано.
+ _Отсутствие контроля перегрузок_ — для приложений с большой пропускной способностью существует шанс вызвать коллапс перегрузок, если только они не реализуют меры контроля на прикладном уровне.

[к оглавлению](#Основы-web)

## Что такое протокол передачи данных? Какие протоколы вы знаете?
__Протокол передачи данных__ — набор соглашений интерфейса логического уровня, которые определяют обмен данными между различными программами. Эти соглашения задают единообразный способ передачи сообщений и обработки ошибок при взаимодействии программного обеспечения разнесённой в пространстве аппаратуры, соединённой тем или иным интерфейсом.

Наиболее известные протоколы передачи данных:

+ HTTP (Hyper Text Transfer Protocol)
+ FTP (File Transfer Protocol)
+ POP3 (Post Office Protocol)
+ SMTP (Simple Mail Transfer Protocol)
+ TELNET (TErminaL NETwork)

[к оглавлению](#Основы-web)

## Что такое _HTTP_ и _HTTPS_? Чем они отличаются?
__HTTP, HyperText Transfer Protocol (Протокол передачи гипертекста)__ — протокол прикладного уровня передачи данных. 

Основой HTTP является технология «клиент-сервер»:

+ _Потребители (клиенты)_, которые инициируют соединение и посылают запрос;
+ _Поставщики (серверы)_, которые ожидают соединения для получения запроса, производят необходимые действия и возвращают обратно сообщение с результатом.

Для идентификации ресурсов HTTP использует глобальные URI. 

HTTP не сохраняет своего состояния. Это означает отсутствие сохранения промежуточного состояния между парами «запрос-ответ».

Структура протокола:

1. _Стартовая строка (starting line)_ — определяет тип сообщения;
2. _Заголовки (headers)_ — характеризуют тело сообщения, параметры передачи и прочие сведения;
3. _Тело сообщения (message body)_ — непосредственно данные сообщения. Обязательно должно отделяться от заголовков пустой строкой.

Заголовки и тело сообщения могут отсутствовать, но стартовая строка является обязательным элементом, так как указывает на тип запроса/ответа.

__HTTPS, HyperText Transfer Protocol Secure__ — расширение протокола HTTP, поддерживающее шифрование. Данные, передаваемые по протоколу HTTPS, «упаковываются» в криптографический протокол SSL или TLS, что обеспечивает защиту от атак, основанных на прослушивании сетевого соединения (при условии, что будут использоваться шифрующие средства и сертификат сервера проверен и ему доверяют).

__Различия _HTTP_ и _HTTPS___:

+ HTTPS является расширением HTTP.

+ HTTP использует не зашифрованное соединение. Соединение по HTTPS поддерживает шифрование.

+ Работа по HTTP быстрей и менее ресурсоёмко, т.к. шифрование HTTPS требует дополнительных затрат.

+ Порты по умолчанию: в случае HTTP это TCP-порт `80`, для HTTPS - TCP-порт `443`.

[к оглавлению](#Основы-web)

## Что такое _FTP_?
__FTP, File Transfer Protocol (Протокол передачи файлов)__ — протокол передачи файлов между компьютерами в сети TCP. С его помощью можно подключаться к FTP-серверам, просматривать содержимое их каталогов и загружать файлы с сервера или на сервер. Протокол построен на архитектуре «клиент-сервер» и использует разные сетевые соединения для передачи команд и данных между клиентом и сервером. 

По умолчанию использует TCP-порт `21`.

[к оглавлению](#Основы-web)

## Чем отличаются методы _GET_ и _POST_?
__GET__ передает данные серверу используя URL, тогда как __POST__ передает данные, используя тело HTTP запроса. Длина URL ограничена 1024 символами, это и будет верхним ограничением для данных, которые можно отослать через GET. POST может отправлять гораздо большие объемы данных. Лимит устанавливается web-server и составляет обычно около 2 Mb.

Передача данных методом POST более безопасна, чем методом GET, так как секретные данные (например пароль) не отображаются напрямую в web-клиенте пользователя, в отличии от URL, который виден почти всегда. Иногда это преимущество превращается в недостатком - вы не сможете послать данные за кого-то другого.

[к оглавлению](#Основы-web)

## Что такое _MIME тип_?
__MIME, Multipurpose Internet Mail Extension (Многоцелевые расширения Интернет-почты)__ — спецификация для передачи по сети файлов различного типа: изображений, музыки, текстов, видео, архивов и др. В HTML указание MIME-типа используется при  передаче данных форм и вставки на страницу различных объектов.

[к оглавлению](#Основы-web)

## Что такое _Web server_?
__Web server (Веб-сервер)__ — сервер, принимающий HTTP-запросы от клиентов и выдающий им HTTP-ответы. Так называют как программное обеспечение, выполняющее функции web-сервера, так и непосредственно компьютер, на котором это программное обеспечение работает. 

Web-серверы могут иметь различные дополнительные функции, например:

+ автоматизация работы web-страниц;
+ ведение журнала обращений пользователей к ресурсам;
+ аутентификация и авторизация пользователей;
+ поддержка динамически генерируемых страниц;
+ поддержка HTTPS для защищённых соединений с клиентами.

Наиболее известные web-серверы:

+ Apache
+ Microsoft IIS
+ nginx

[к оглавлению](#Основы-web)

## Что такое _Web application_?
__Web application (Веб-приложение)__ - клиент-серверное приложение, в котором клиентом выступает браузер, а сервером — web-сервер. Логика web application распределена между сервером и клиентом, хранение данных осуществляется, преимущественно, на сервере, а обмен информацией происходит по сети. Одним из преимуществ такого подхода является тот факт, что клиенты не зависят от конкретной операционной системы пользователя, поэтому web application является кроссплатформенным сервисом.

[к оглавлению](#Основы-web)

## Что такое _Application server_?
__Application Server (Сервер приложений)__ — программа, представляющая собой сервер, который занимается системной поддержкой приложений и обеспечивает их жизненный цикл в соответствии с правилами, определёнными в спецификациях. Может работать как полноценный самостоятельный web-сервер или быть поставщиком страниц для другого web-сервера. Обеспечивает обмен данными между приложениями и клиентами, берёт на себя выполнение таких функций, как создание программной среды для функционирующего приложения, идентификацию и авторизацию клиентов, организацию сессии для каждого из них.

Наиболее известные серверы приложений Java:

+ Apache Tomcat
+ Jetty
+ JBoss
+ GlassFish
+ IBM WebSphere
+ Oracle Weblogic

[к оглавлению](#Основы-web)

## Чем отличаются _Web server_ и _Application server_?
Понятие web server относится скорее к способу передачи данных (конкретно, по протоколу HTTP), в то время как понятие Application server относится к способу выполнения этих самых приложений (конкретно, удаленная обработка запросов клиентов при помощи каких-то программ, размещенных на сервере). Эти понятия нельзя ставить в один ряд. Они обозначают разные признаки программы. Какие-то программы удовлетворяют только одному признаку, какие-то - нескольким сразу.

Apache Tomcat умеет выполнять приложения? Да, значит он является application server. Apache Tomcat умеет отдавать данные по HTTP? - Да. Следовательно он является web server.

Возьмите какую-нибудь базу данных, в которой на хранимых процедурах описана сложная логика и можно в ответ на SQL-запросы отправлять даже sms. Такую базу данных можно назвать application server, но web server - уже нет, потому что все это не работает с клиентом по HTTP протоколу.

Возьмите чистый Apache, в котором не включены никакие модули для поддержки языков программирования. Он умеет отдавать только статичные файлы и картинки по протоколу HTTP. Это web server, но не application server. Включите модуль для поддержки PHP и разместите там программу на PHP, которая делает запросы к базе данных и динамически формирует страницы. Теперь Apache стал и application server.

[к оглавлению](#Основы-web)

## Что такое _AJAX_? Как принципиально устроена эта технология?
__AJAX, Asynchronous Javascript and XML (Асинхронный Javascript и XML)__ — подход к построению интерактивных пользовательских интерфейсов web-приложений, заключающийся в «фоновом» обмене данными браузера и web-сервера. В результате, при обновлении данных web-страница не перезагружается полностью и web-приложения становятся быстрее и удобнее.

При использовании AJAX:

1. Пользователь заходит на web-страницу и взаимодействует с каким-нибудь её элементом.
2. Скрипт на языке JavaScript определяет, какая информация необходима для обновления страницы.
3. Браузер отправляет соответствующий запрос на web-сервер.
4. Web-сервер возвращает только ту часть документа, на которую пришёл запрос.
5. Скрипт вносит изменения с учётом полученной информации (без полной перезагрузки страницы).

AJAX базируется на двух основных принципах:

1. использование технологии динамического обращения к серверу «на лету» (без перезагрузки страницы полностью) через динамическое создание:
    + _дочерних фреймов_;
    + _тега `<script>`_;
    + _тега `<img>`_.
2. использование _DHTML_ для динамического изменения содержания страницы;

AJAX не является самостоятельной технологией, это концепция использования нескольких смежных технологий:

+ _(X)HTML_, _CSS_ для подачи и стилизации информации;
+ _DOM-модель_, операции над которой производятся Javascript на стороне клиента, для обеспечения динамического отображения и взаимодействия с информацией;
+ _XMLHttpRequest_ или другой транспорт (_IFrame_, _SCRIPT-тег_, _..._) для асинхронного обмена данными с web-сервером;
+ _JSON_ или любой другой подходящий формат (_форматированный HTML_, _текст_, _XML_, _..._) для обмена данными.

[к оглавлению](#Основы-web)

## Что такое _WebSocket_?
__WebSocket__ — протокол полнодуплексной связи поверх TCP-соединения, предназначенный для обмена сообщениями между браузером и web-сервером в режиме реального времени.

Протокол _WebSocket_ определяет две URI схемы

+ `ws:` - нешифрованное соединение
+ `wss:` - шифрованное соединение

[к оглавлению](#Основы-web)

## Что такое _JSON_?
__JSON, JavaScript Object Notation__ — текстовый формат обмена данными, основанный на JavaScript.

JSON представляет собой (в закодированном виде) одну из двух структур:

+ _Набор пар «ключ:значение»_;
+ _Упорядоченный набор значений_.

Ключом может быть только строка (регистрозависимая: имена с буквами в разных регистрах считаются разными).

В качестве значений могут быть использованы:

+ _Объект_ — неупорядоченное множество пар «ключ:значение», заключённое в фигурные скобки `{ }`. Ключ описывается строкой, между ним и значением стоит символ `:`. Пары ключ-значение отделяются друг от друга запятыми;
+ _Массив (одномерный)_ — упорядоченное множество значений. Массив заключается в квадратные скобки `[ ]`. Значения разделяются запятыми.
+ _Число_;
+ _Литералы_ `true`, `false` и `null`;
+ _Строка_ — упорядоченное множество из нуля или более символов Unicode, заключенное в кавычки `" "`. Символы могут быть указаны с использованием escape-последовательностей, начинающихся с обратной косой черты `\`, или записаны шестнадцатеричным кодом в кодировке UTF-8 в виде `\uFFFF`.

[к оглавлению](#Основы-web)

## Что такое _JSON схема_?
__JSON Schema__ — один из языков описания структуры JSON-документа, используя синтаксис JSON.

Это самоописательный язык: при его использовании для обработки данных и описания их допустимости могут использоваться одни и те же инструменты сериализации/десериализации.

[к оглавлению](#Основы-web)

## Что такое _cookies_?
__Сookies («куки»)__ — небольшой фрагмент данных, отправленный web-сервером и хранимый на устройстве пользователя. Всякий раз при попытке открыть страницу сайта, web-клиент пересылает соответствующие этому сайту cookies web-серверу в составе HTTP-запроса. Применяется для сохранения данных на стороне пользователя и на практике обычно используется для:

+ аутентификации пользователя;
+ хранения персональных предпочтений и настроек пользователя;
+ отслеживания состояния сеанса доступа пользователя;
+ ведения разнообразной статистики.

[к оглавлению](#Основы-web)

## Что такое _«сессия»_?
__Сессия__ – промежуток времени между первым и последним запросами, которые пользователь отправляет со своего устройства на сервер сайта. Завершается сессия в случае, если со стороны пользователя не поступало запросов в течение определенного промежутка времени или же при обрыве связи.

[к оглавлению](#Основы-web)

## Что такое _«авторизация»_ и _«аутентификация»_? Чем они отличаются?
__Аутентификация__ - это проверка соответствия субъекта и того, за кого он пытается себя выдать, с помощью некой уникальной информации (отпечатки пальцев, цвет радужки, голос и тд.), в простейшем случае - с помощью имени входа и пароля.

__Авторизация__ - это проверка и определение полномочий на выполнение некоторых действий (например, чтение файла) в соответствии с ранее выполненной аутентификацией.

Очевидно, что это разные понятия, но при этом без первого не может быть второго и наоборот. То есть имея разрешение на работу, вы не сможете оказаться на рабочем месте без предъявления пропуска, равно как и нет смысла в демонстрации пропуска, если вы не планируете работать. Именно тот факт, что одного не бывает без другого, и вызывает у людей заблуждение, что это одно и то же.

[к оглавлению](#Основы-web)

#Источники
+ [Википедия](https://ru.wikipedia.org/)