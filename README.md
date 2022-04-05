# Django-chat
Real time chat on Django (channels). I implemented this project using special library "channels" which allows to work with websockets. For the frontpage part of this project i used css framework "Tailwind". 

## Discription

In this project I have implemented the following things:

    1. Model of rooms which u can change in Django admin panel
    2. User regestration and sign in by UserCreationForm and User model (also an option to log out of the account using the auth_views module)
    3. Sending and accepted messages inside room in real time.

I used the standard Sqlite database, which is installed by Django by default. All the messages in my chat saved in memory channel layer. You can connect Redis database instead by changing the parameter in settings:

```python
CHANNEL_LAYERS = {
    'default': {
        'BACKEND': 'channels.layers.InMemoryChannelLayer'
        }
}
```


## To use this project follow these steps:

  1. Create your working environment (python3 -m venv chatvenv)
  2. Install Django (4.0.2), channels(3.0.4)
  4. Run app (python3 manage.py runserver)

