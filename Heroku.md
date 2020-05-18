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