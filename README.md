# FileFormatter

В настоящее время дизайнерам интерьеров приходится тратить много времени на ручное создание каждого договора, вставку необходимых данных и подготовку текстовых документов. Этот процесс является трудоемким и рутинным, так как требует повторения одних и тех же операций для каждого договора. Каждый дизайнер может использовать свои собственные форматы и шаблоны договоров, что затрудняет стандартизацию и последующую автоматизацию процесса их создания.

Для решения данной проблемы необходимо разработать веб-систему, которая будет облегчать процесс заключения договоров между дизайнером и клиентами, а также обеспечивать удобный и безопасный способ управления договорами и клиентскими данными. Для четкого понимания функционального наполнения системы и технологий разработки ниже прилагаются: 

* [Функциональное задание](#функциональное-задание)
* [Техническое задание](#техническое-задание)

## Функциональное задание

Данный раздел описывает возможности пользователя в контексте работы системы.

1. Управление договорами и клиентами:

Веб-интерфейс должен позволять создавать записи о договорах, клиентах и объектах.
Пользователи должны иметь возможность выбирать тип объекта объекта (например, квартира) и вводить соответствующие данные для клиента (ФИО, эл. почта, пол и т.д.) и объекта (цена, адрес, акты закрытия, календарные планы и т.д.).
Должна быть возможность просматривать, редактировать и удалять существующие записи.
Дизайнеры должны иметь возможность вносить изменения в данные записи.

2. Генерация готовых текстов (акты, письма, договора):

Система должна использовать клиентские данные для внесения в шаблоны документов с дальнейшей генерацией договора в документ формата ".pdf".
Пользователи должны иметь возможность заполнять поля шаблонов договоров и актов закрытия с помощью ввода соответствующих входных данных (контакты клиента, банковские реквизиты клиента и т.д.).
Сгенерированные договоры и акты закрытия должны быть доступны для просмотра, редактирования и загрузки.

3. Управление текстами документов (письма, тексты договоров и т.д.):

Система должна предоставлять возможность создавать тексты писем на основе данных договоров и актов закрытия.
Пользователи должны иметь возможность редактировать тексты писем и отправлять их клиентам через систему.
Должна быть возможность сохранения и просмотра истории отправленных писем.


## Техническое задание

Данный раздел описывает инструменты разработки системы. Этапы разработки разделены на 3 слоя с описанием необходимых сервисов для разработки.

1. Фронтенд:

Разработать веб-интерфейс с использованием NocoDB.
Обеспечить создание и редактирование договоров, просмотр договоров, актов закрытия и текстов писем.
Реализовать формы для ввода данных пользователей, объектов работы и входных данных договоров.
Обеспечить возможность загрузки и скачивания договоров, актов закрытия и текстов писем.

2. Бэкенд: 

Разработать серверную часть.
Реализовать взаимодействие с API для обмена данными между пользователем и сервером.
Создать базу данных для хранения информации о пользователях, договорах, актах закрытия и текстах писем.
Разработать логику генерации договоров и актов закрытия на основе шаблонов и входных данных с помощью шины для создания рабочих процессов N8N и с учетом версии соответвствующих шаблонов формата MarkDown и LaTex, хранящихся на GitLab.
Разработать функцию вставки готовой подписи исполнителя, хранящейся в виде изображения в формате ".png", в генерируемый документ в соответствующее поле для подписи.

3. Хранение данных:

Обеспечить взаимодействие с Nextcloud для хранения и доступа к файлам (договоры, акты закрытия и т.д.) и изображениям.
Реализовать механизм автоматического сохранения и загрузки файлов на Nextcloud.
На базе NocoDB спроектировать структуру базы данных для хранения соответвующей информации о клиентах и объектах из полей ввода с учетом нормализованных форм отношения, обеспечить хранение. Пример структуры данных находится [по ссылке](https://docs.google.com/spreadsheets/d/1FhZs1RxUTdo9KgK4eRTbrZJkKmiv1ncx-Pp_n-4FeJc/edit?usp=sharing).
