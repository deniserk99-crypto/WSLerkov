\
В качестве ОС реомендую выбрать ubuntu 22.04/24.04. Скриншоты с последовательным описанием работы добавлять в файл .md (Markdown - синтаксис изучить самостоятельно), итоговый файл и вложения - в публичный гит-репозиторий. Ссылку на него прикладываете в качестве ответа на задание.

# Установка WSL, Ubuntu, Python и PostgreSQL

## 1. Цель работы
Установить WSL,Ubuntu,Python,PostgreSQL.

##2. Установка и проверка Ubuntu

Установка дистрибутива Ubuntu 24.04 выполнена с помощью WSL. После запуска создан пользователь Linux .
Скриншот: screenshots/01-ubuntu.png

## 3. Установка Python

Python и необходимые инструменты установлены командами:

sudo apt update
sudo apt install -y python3 python3-pip python3-venv

Версии проверены командами:

python3 --version
pip3 --version

![Установка Ubuntu и Python](screenshots/01-python-install.png)


##4. Установка PostgreSQL

PostgreSQL установлен командой:

sudo apt install -y postgresql postgresql-contrib

Сервер запущен командой:

sudo service postgresql start

Проверка состояния и версии выполнена командами:

sudo service postgresql status
sudo -u postgres psql -c "SELECT version();"

Результат: PostgreSQL 16.15, сервер работает на порту 5432.

![Установка PostgreSQL](screenshots/02-postgresql-install.png)

##5. Проверка Python

Создан файл main.py, который выводит приветствие, версию Python и название операционной системы.

Запуск программы:

python3 main.py

Ожидаемый результат: программа выводит сообщение Hello from Ubuntu on WSL!, версию Python и название операционной системы Linux.

![Проверка Python](screenshots/03-python-test.png)



