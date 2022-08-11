Vector-role
=========

Устанвливает Vector на систему Centos 7

Requirements
------------

Роль работает только на ОС CentOS 7. В файле конфигурации vector (vector.yml.j2) необходимо указать адрес сервера базы данных clickhouse.

Role Variables
--------------

| Переменная  | Назначение  |
|:---|:---|
| vector_version | задает версию дистрибутива |
| arch | задает архитектуру дистрибутива |
| vector_config_dir | указывает каталог для хранения конфигурации |

Example Playbook
----------------

```yml
- name: Install Vector
  hosts: vector
  remote_user: centos
  roles:
    - vector-role
```

License
-------

MIT

Author Information
------------------

Розум Сергей
