# Django-chat
Real time chat on Django (channels). I implemented this project using special library "channels" which allows to work with websockets. For the frontpage part of this project i used css framework "Tailwind". 

## Discription

I used the standard Sqlite database, which is installed by Django by default. All the messages in my chat saved in memory channel layer. You can connect Redis instead by changing the parameter in settings:
> CHANNEL_LAYERS = {
    'default': {
        'BACKEND': 'channels.layers.InMemoryChannelLayer'
        }
}
>

## To use this project follow these steps:

  1. Create your working environment (python3 -m venv chatvenv)
  2. Install Django (4.0.2), channels(3.0.4)
  4. Run app (python3 manage.py runserver)

