# FileFormatter

В настоящее время дизайнерам приходится тратить много времени на ручное создание каждого договора, вставку необходимых данных и подготовку текстовых документов. Это процесс является трудоемким и рутинным, так как требует повторения одних и тех же операций для каждого договора. Каждый дизайнер может использовать свои собственные форматы и шаблоны договоров, что затрудняет стандартизацию и последующую автоматизацию процесса их создания.

Для решения данной проблемы необходимо разработать веб-систему, целью которой будет является облегчение процесса заключения договоров между дизайнером и клиентами, а также обеспечение удобного и безопасного способа управления договорами и клиентскими данными.

* [Функциональное задание](#функциональное-задание)
* [Техническое задание](#FZ)

## Функциональное задание:

Управление договорами:

Веб-интерфейс должен позволять пользователям добавлять новые договоры в систему.
Пользователи должны иметь возможность выбирать тип объекта работы (например, квартира) и вводить соответствующие данные (цена, адрес, акты закрытия, календарные планы и т. д.).
Должна быть возможность просматривать, редактировать и удалять существующие договоры.
Пользователи должны иметь возможность вносить изменения в данные договоров.

Генерация договоров и актов закрытия:

Система должна использовать шаблонизированный текстовой формат (.md и LaTeX) для генерации договоров и актов закрытия на основе входных данных.
Пользователи должны иметь возможность заполнять поля шаблонов договоров и актов закрытия с помощью ввода соответствующих входных данных (например, паспортные данные, ФИО, телефон, банковские реквизиты).
Сгенерированные договоры и акты закрытия должны быть доступны для просмотра, редактирования и загрузки.

Управление текстами писем:

Система должна предоставлять возможность создавать тексты писем на основе данных договоров и актов закрытия.
Пользователи должны иметь возможность редактировать тексты писем и отправлять их клиентам через систему.
Должна быть возможность сохранения и просмотра истории отправленных писем.


## <a id="FZ"></a>Техническое задание:

Фронтенд:

Разработать веб-интерфейс с использованием HTML, CSS и JavaScript.
Обеспечить создание и редактирование договоров, просмотр договоров, актов закрытия и текстов писем.
Реализовать формы для ввода данных пользователей, объектов работы и входных данных договоров.
Обеспечить возможность загрузки и скачивания договоров, актов закрытия и текстов писем.

Бэкенд:

Разработать серверную часть.
Реализовать API для обмена данными между фронтендом и бэкендом.
Создать базу данных для хранения информации о пользователях, договорах, актах закрытия и текстах писем.
Разработать логику генерации договоров и актов закрытия на основе шаблонов и входных данных.

Интеграция с Nextcloud:

Обеспечить взаимодействие с Nextcloud для хранения и доступа к файлам (договоры, акты закрытия и т. д.).
Реализовать механизм автоматического сохранения и загрузки файлов на Nextcloud с учетом требований безопасности.

Безопасность:

Обеспечить безопасное хранение и передачу информации между клиентом и сервером.
Реализовать механизмы аутентификации и авторизации пользователей с учетом требований безопасности.

Хранение данных:

Данные, включая договоры, акты закрытия и тексты писем, должны храниться на Nextcloud для обеспечения безопасности и доступности.
Система должна обеспечивать защищенное хранение данных с учетом требований безопасности ГОСТ 34.

## БД (сущности и отношения)
