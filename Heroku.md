## Heroku


**Login:**
```heroku
heroku login
```


**Adding SSH Key into the project that is already present in system:**
```heroku
heroku keys:add
```


**Creating Heroku App:**
```heroku
heroku create <appname>(optional)
```


**Logs i.e. history**
```heroku
heroku logs
```


If getting error due to **static files(django specific)** then do:
```heroku
heroku config:set DISABLE_COLLECTSTATIC=1
```


**Pushing code to git repo**
```heroku
git push heroku master
```

**restart heroku app**
```heroku
heroku restart
```

-----------------------------------------------------

## Inside Django Project:

```
pip install django-heroku 
pip install gunicorn
pip install python-decouple
```
#if heroku shows some error(in ubuntu),then
```
sudo apt install libpq-dev
```

In Setting.py:

```python
import django_heroku
from decouple import config
import dj_database_url
```

create a file .env:
keep SECRET_KEY their 

and in settings.py:
```
SECRET_KEY = config('SECRET_KEY')
```

middleware:
```
middleware: 'whitenoise.middleware.WhiteNoiseMiddleware',
```

staticfiles:
```
STATICFILES_DIRS = [os.path.join(BASE_DIR, 'static')]
STATICFILES_STORAGE='whitenoise.storage.CompressedManifestStaticFilesStorage'
```
locals:
```
django_heroku.settings(locals())
```

```
DATABASES['default'] = dj_database_url.config(default='<URI from heroku-django addons > setting>')

db_from_env = dj_database_url.config(conn_max_age=600)
DATABASES['default'].update(db_from_env)
```

------------------------------------------------
create file Procfile:
```
web: gunicorn <projectname>.wsgi
```

------------------------------------------------
create file requirements.txt:
Use command:

```
pip freeze > requirements.txt
```
--------------------------------------------------------------
SECRET_KEY needs to be added into settings from heroku dashboard of the app


Add remote to git of heroku:
```
git remote add heroku <https://git.heroku.com/<heroku-project-name>.git>
```

Pushing to git heroku
```
git push heroku master
```
------------------------------------------------------------
To run any command use 
```heroku
heroku run <command>
```
eg:
```heroku
heroku run python manage.py runserver
heroku run python manage.py makemigrations
heroku run python manage.py createsuperuser





```
