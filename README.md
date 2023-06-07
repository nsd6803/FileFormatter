# FileFormatter

В настоящее время дизайнерам приходится тратить много времени на ручное создание каждого договора, вставку необходимых данных и подготовку текстовых документов. Это процесс является трудоемким и рутинным, так как требует повторения одних и тех же операций для каждого договора. Каждый дизайнер может использовать свои собственные форматы и шаблоны договоров, что затрудняет стандартизацию и последующую автоматизацию процесса их создания.

Для решения данной проблемы необходимо разработать веб-систему, которая будет облегчать процесс заключения договоров между дизайнером и клиентами, а также обеспечивать удобный и безопасный способ управления договорами и клиентскими данными.

* [Функциональное задание](#функциональное-задание)
* [Техническое задание](#техническое-задание)

## Функциональное задание:

1. Управление договорами:

Веб-интерфейс должен позволять дизайнерам добавлять новые договоры в систему.
Пользователи должны иметь возможность выбирать тип объекта работы (например, квартира) и вводить соответствующие данные (цена, адрес, акты закрытия, календарные планы и т. д.).
Должна быть возможность просматривать, редактировать и удалять существующие договоры.
Дизайнеры должны иметь возможность вносить изменения в данные договоров.

2. Генерация договоров и актов закрытия:

Система должна использовать шаблонизированный текстовой формат (.md и LaTeX) для генерации договоров и актов закрытия на основе входных данных.
Пользователи должны иметь возможность заполнять поля шаблонов договоров и актов закрытия с помощью ввода соответствующих входных данных (например, паспортные данные, ФИО, телефон, банковские реквизиты).
Сгенерированные договоры и акты закрытия должны быть доступны для просмотра, редактирования и загрузки.

3. Управление текстами писем:

Система должна предоставлять возможность создавать тексты писем на основе данных договоров и актов закрытия.
Пользователи должны иметь возможность редактировать тексты писем и отправлять их клиентам через систему.
Должна быть возможность сохранения и просмотра истории отправленных писем.


## Техническое задание:

1. Фронтенд:

Разработать веб-интерфейс с использованием NoCode решения.
Обеспечить создание и редактирование договоров, просмотр договоров, актов закрытия и текстов писем.
Реализовать формы для ввода данных пользователей, объектов работы и входных данных договоров.
Обеспечить возможность загрузки и скачивания договоров, актов закрытия и текстов писем.

2. Бэкенд:

Разработать серверную часть.
Реализовать API для обмена данными между фронтендом и бэкендом.
Создать базу данных для хранения информации о пользователях, договорах, актах закрытия и текстах писем.
Разработать логику генерации договоров и актов закрытия на основе шаблонов и входных данных с помощью шины для создания рабочих процессов N8N.

3. Хранение данных:

Обеспечить взаимодействие с Nextcloud для хранения и доступа к файлам (договоры, акты закрытия и т. д.).
Реализовать механизм автоматического сохранения и загрузки файлов на Nextcloud с учетом требований безопасности. Пример базы данных находится [по ссылке]().

4. Безопасность:

Обеспечить безопасное хранение и передачу информации между клиентом и сервером.
