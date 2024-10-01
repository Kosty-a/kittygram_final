![Main Kittygram workflow](https://github.com/Kosty-a/kittygram_final/actions/workflows/main.yml/badge.svg)

## Описание проекта Kittygram

Проект Kittygram представляет собой небольшой сайт, на котором можно:
- добавить котика, указав данные о нём:
  - фото;
  - имя;
  - год рождения;
  - один из предустановленных цветов;
  - достижения.
- посмотреть данные об уже добавленных другими пользователям котиках;
- зарегистрироваться (доступ к котиками возможен только для зарегистрированных пользователей).

Адрес сайта: `https://kitty-gram.work.gd`

## Стек использованных технологий

- Django и Django REST Framework;
- PostgreSQL;
- Node JS;
- Nginx;
- Docker;
- GitHub actions.

## Как развернуть проект

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:Kosty-a/kittygram_final.git
```

```
cd backend
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

* Если у вас Linux/macOS

    ```
    source env/bin/activate
    ```

* Если у вас windows

    ```
    source env/scripts/activate
    ```

Обновить пакетный менеджер pip:

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить сервер разработки Django:

```
python3 manage.py runserver
```

Для разворачивания проекта на удалённом сервере необходимо:
- создать на удалённом сервере целевую папку и файл `.env`;
- заполнить файл `.env` по образцу;
- поменять данные в файле `main.yml`;
- сделать push в ветку `main`.

## Как заполнить файл `.env`

В корне репозитория расположен файл `.env.example` с примером содержимого файла `.env`.

- `SECRET_KEY`: секретный ключ Django-проекта;
- `DEBUG`: `True` или `False` - активация/деактивация режима разработки;
- `ALLOWED_HOSTS`: разрешённые хосты;
- `SQLITE`: если переменная пустая или её нет, то в проекте будет использоваться PostgreSQL, в противном случае SQLite;
- `POSTGRES_USER`: логин для БД (здесь и ниже данные для PostgreSQL);
- `POSTGRES_PASSWORD`: пароль для БД;
- `POSTGRES_DB`: имя БД;
- `DB_HOST`: имя контейнера с БД;
- `DB_PORT`: порт, на которм запущен сервер БД.

## Автор проекта
Демин Константин
