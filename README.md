# Django-chat
Чат в реальном времени на Django. Я реализовал этот проект, используя специальную библиотеку "channels", которая позволяет работать с websockets.

## Описание

В этом проекте я реализовал следующие вещи:

    1. Модель комнат, которую вы можете изменить в админ-панели Django
    2. Регистрация пользователя и вход в систему с помощью UserCreationForm и модели пользователя (также есть возможность выхода из учетной записи с помощью модуля auth_views)
    3. Отправка и принятие сообщений внутри комнаты в режиме реального времени.

Я использовал стандартную базу данных Sqlite, которая по умолчанию установлена Django. Все сообщения в моем чате сохраняются на канальном уровне памяти. Вместо этого вы можете подключить базу данных Redis, изменив параметр в настройках:

```python
CHANNEL_LAYERS = {
    'default': {
        'BACKEND': 'channels.layers.InMemoryChannelLayer'
        }
}
```

Установка:
--
```
$ git clone https://github.com/qvog/django-ecommerce.git
$ cd django-ecommerce
$ pip install -r requirements.txt
```

> Сделайте настройку собственной базы данных! 

Миграции и создание супер-пользователя.
```
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

> Используйте адрес: http://127.0.0.1:8000/ (Для проверки) 

