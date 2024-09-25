Role Name
=========

Данная роль устанавливает Vector на debian-based машины, и настраивает его на работу с clickhouse-сервером, а также устанавливает nginx для тестового сбора логов.

Requirements
------------

Ansible >= 2.17 (скорее всего работает и на более ранних версиях, протестировано только на этой)
Подготовленный clickhouse-сервер.

Role Variables
--------------

В main.yml

| Переменная | Значение по умолчанию | Описание |
| :----: | :---: | :-------: |
| clickhouse_addr | - | Адрес clickhouse-сервера |
| database_name | - |Название базы данных в clickhouse, в которую будут посылаться логи|
| table_name | - |Название таблицы, в которую будут посылаться логи|

В secrets.yml

| Переменная | Значение по умолчанию | Описание |
| :----: | :---: | :-------: |
| username | - | Имя пользователя для БД clickhouse |
| password | - | Пароль для пользователя БД clickhouse |

Dependencies
------------

-

Example Playbook
----------------

  hosts: vector
  roles:
    - vector

License
-------

MIT

Author Information
------------------

Matvey Makhnin