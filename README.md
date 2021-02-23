Vagrantfile для установки Postgres 8.4 на Ubuntu 18.04 

## Зивисимости

Для работы необходимо наличие следующих программ

* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](http://vagrantup.com/)

## Использование

Склонировать репозиторий в нужную вам директорию

Запустить
```sh
vagrant up
```

Подключиться по SSH
```sh
vagrant ssh
sudo su - postgres
```

Остановить и удалить
```sh
vagrant destroy
```