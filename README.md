# Api_final

## Описание

Реализация API учебного проекта Yatube согласно принципам REST.
Осуществлена возможность делать различные запросы к API Yatube, учитывая аутентификацию пользователя.
С помощью API можно:
Смотреть, писать, редактировать и удалять посты.
Комментировать посты, а так-же читать, редактировать и удалять комментарии.
Создавать сообщества и просматривать информацию о них.
Подписываться на авторов.

## Технологии

- Python 3
- Django==2.2.16
- Django REST Framework==3.12.4
- Django REST Framework-simplejwt==4.7.2

### Как запустить проект

Клонировать репозиторий и перейти в него в командной строке:

$ git clone https://github.com/AndrejGurtovoj/api_final_yatube.git

$ cd api_final_yatube
Cоздать и активировать виртуальное окружение:

$ python -m venv venv
$ . venv/Scripts/activate
Установить зависимости из файла requirements.txt:

$ python -m pip install --upgrade pip
$ pip install -r requirements.txt
Выполнить миграции:

$ python manage.py migrate
Запустить проект:

$ python manage.py runserver

### Управление пользователями

Описание работы и примеры
После запуска сервера документация находится по адресу:

http://127.0.0.1:8000/redoc/

Примеры запросов к API
Получить список всех публикаций:

GET-запрос
http://127.0.0.1:8000/api/v1/posts/
Создать публикацию:

POST-запрос
http://127.0.0.1:8000/api/v1/posts/
Создать комментарий к публикации с ID=1:

POST-запрос
http://127.0.0.1:8000/api/v1/posts/1/comments/
Получение JWT токенов
Работа с опасными методами API возможна только с помощью JWT токенов.

Получить JWT-токен

POST-запрос
http://127.0.0.1:8000/api/v1/jwt/create/

