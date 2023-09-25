**Архитектура ПО (семинары)**

***HomeWork 10. Структура приложения с пользовательским интерфейсом и базой данных (паттерн Repository)***

Вы можете реализовать эти патерны, в рамках своего проекта, к которому Вы делали диограммы и таблицы. Или реализовать отдельно от них.

Домашнее задание: Реализация паттернов Агрегатор, Репозиторий и Кеширования

Цель: Освоить принципы работы и применение трёх ключевых паттернов проектирования: Агрегатор, Репозиторий и Кеширование.

Часть 1: Паттерн Агрегатор
Реализуйте классы Order, OrderItem и Product.

Order должен содержать список OrderItem, каждый из которых содержит Product и количество этого продукта.

У каждого заказа должен быть метод для расчета общей стоимости.

Часть 2: Паттерн Репозиторий
Создайте интерфейс OrderRepository, который определяет методы для работы с заказами (сохранение, загрузка по ID, загрузка всех заказов и т. д.).

Реализуйте класс OrderRepositoryImpl, который реализует данный интерфейс, используя любую базу данных на ваш выбор (может быть встроенной, например, SQLite).

В репозитории обеспечьте сохранение и загрузку заказов, а также всех связанных с ними объектов (OrderItem, Product).

Часть 3: Паттерн Кеширования
Исследуйте и выберите одну из библиотек для кеширования в Java (например, EhCache, Caffeine или Guava Cache).

Реализуйте кеширование в вашем репозитории таким образом, чтобы часто запрашиваемые заказы загружались из кэша, а не из базы данных.

Обеспечьте инвалидацию кэша (обновление данных в кэше), если информация в базе данных была изменена.

Дополнительное задание:

Реализуйте пользовательский интерфейс (может быть консольным или графическим), чтобы демонстрировать создание, редактирование, загрузку и удаление заказов.

Добавьте возможность фильтрации и сортировки заказов при их загрузке из базы данных.

Советы:

Соблюдайте принципы SOLID при проектировании и реализации вашего приложения.

Обрабатывайте все возможные исключения, особенно при работе с базой данных.

Подумайте над оптимальной стратегией кеширования в зависимости от предполагаемого объема данных и частоты запросов.

Это задание предполагает разработку приложения с использованием трёх ключевых паттернов




***HomeWork 11. Сервис-ориентированные архитектуры***

Расширяем наш проект

Была одна главная страница- делаем наброски для друг страниц(Заказ, доставка, и т д в зависимости от темы.

 Пример - https://stealth-force-e00.notion.site/f38d6a54d65542fd97f8fc39aba36758?pvs=4). Вы это делаете для дизайнера, можно сделать и в пейнт, не надо тратить на это много время . https://www.figma.com/

Расширяем диограммы.

Пример на основе приложения для робота-пылесоса - https://geekbrainspro.notion.site/2-11-1b0361e053584d5db3f09064ef90cf2d

__
UML-диаграмма пакетов:
__

Пакеты и подсистемы: Показывает структуру пакетов и их взаимосвязи. Пакеты могут содержать классы, интерфейсы, диаграммы и другие элементы.

Отношения между пакетами: Диаграмма может показать, как пакеты связаны друг с другом, например, зависимости или ассоциации.

__


UML-диаграмма системы обновления приложения:
__

Компоненты и связи: Показывает компоненты, связанные с обновлением приложения, такие как "Клиентское приложение", "Сервер обновлений", "База данных версий".

Поток данных: Может включать поток данных от клиентского приложения к серверу обновлений и обратно.
__

UML-диаграмма домена (Domain Diagram):

__

Сущности и связи: Диаграмма домена обычно представляет ключевые сущности в системе и связи между ними. Это может быть базовая структура данных, которая влияет на всю систему.

Атрибуты: Диаграмма может также включать атрибуты, которые описывают каждую сущность.

Системы и компоненты: Если система состоит из различных подсистем или компонентов, они также могут быть показаны

__

UML-диаграмма системы обновления приложения:

Компоненты и связи: Показывает компоненты, связанные с обновлением приложения, такие как "Клиентское приложение", "Сервер обновлений", "База данных версий".

Поток данных: Может включать поток данных от клиентского приложения к серверу обновлений и обратно.

__
__
__
__

По желанию, но крайне рекомендуется добавить к своему проекту.

Спроектировать слой  API Gateway (mobile, web), сформировать REST запросы: GET, POST, PUT, DELETE (https://swagger.io).

Предположим, у вас есть простой API для управления списком пользователей. Вам нужно описать запрос типа GET, который вернет список всех пользователей.

__

Откройте Swagger: Перейдите на сайт https://swagger.io и, возможно, создайте новую спецификацию или проект, чтобы начать описание вашего API.

____

Описание запроса GET:
Определите функциональность API Gateway:

__

Определите, какие функции будет выполнять ваш API Gateway. Например, это может быть маршрутизация запросов от мобильных устройств и веб-клиентов к соответствующим микросервисам.

Выберите инструмент Swagger:

__

Откройте инструмент Swagger (https://swagger.io) или его альтернативы, которые позволяют создавать и документировать API.

Создайте новую спецификацию:

__

Если используете Swagger, создайте новую спецификацию (или проект) для вашего API Gateway.
Определите эндпоинты:

__

Определите список эндпоинтов (URL-путей), которые будут доступны через ваш API Gateway. Например, /mobile и /web.
Сформируйте запросы:

__

Для каждого эндпоинта, определите HTTP-методы, которые он поддерживает (GET, POST, PUT, DELETE).
Опишите запросы:

__

Для каждого метода опишите, какие параметры (если есть) должны быть переданы в запросе, а также форматы данных запроса и ответа.
Пример запроса:

__

Предоставьте пример запроса для каждого метода, чтобы пользователи могли понять, как правильно формировать запросы.
Форматы данных:

__

Укажите, какой формат данных (обычно JSON) используется для передачи данных между клиентами и API Gateway.
Генерируйте документацию:

__

Используйте возможности инструмента Swagger для автоматической генерации документации на основе вашей спецификации. Документация должна быть понятной и информативной.
Тестирование:

__

Используйте инструмент Swagger или другие инструменты для тестирования запросов на вашем API Gateway. Убедитесь, что запросы выполняются корректно.
Документация и доступность:

__

Предоставьте ссылку на документацию вашего API Gateway. Удостоверьтесь, что другие разработчики и клиенты смогут получить доступ к этой документации.

__

Помните, что проектирование API Gateway - это описание, как клиенты (мобильные приложения, веб-приложения и т.д.) будут взаимодействовать с вашей системой через единый входной точки. Swagger поможет вам создать четкую документацию, которая упростит интеграцию с вашим API Gateway.

Пример выполнения - https://stealth-force-e00.notion.site/289383d7b8b3424f911c04b25d722c80?pvs=4

__

Задача Swagger - упростить процесс описания и документирования вашего API, а также предоставить средства для тестирования API непосредственно из документации.


***HomeWork 12. Принципы тестирования приложений***

Робот пылесос - это ПРИМЕР!

Продолжаем свой проект. Заполняем документацию для тестов по примеру.

https://geekbrainspro.notion.site/10-12-824e24672d0242f8b05bb34c842d7aca