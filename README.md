# Static Site for NetCS Lab Edit

A start template for Django

## Features

- Production-ready configuration for Static Files, Database Settings, Gunicorn, etc.
- Enhancements to Django's static file serving functionality via WhiteNoise.
- Latest **Python 3.6** runtime environment. 

## 1. Initial Project

### 1.1. Creating Your Environment

    $ pip install virtualenv
    $ pip install virtualenvwrapper
    $ vim .bashrc
    export WORKON_HOME=$HOME/.virtualenvs
    export PROJECT_HOME=$HOME/Devel
    source /usr/local/bin/virtualenvwrapper.sh
    $ mkvirtualenv netcs

#### Useful Commands for Virtualenvwrapper

    # show vitualenv list
    $ lsvirtualenv
    
    # make virtualenv
    $ mkvirtualenv [env_name]
    
    # enter virtualenv
    $ workon [env_name]
    
    # exit virtualenv
    $ deactivate
    
    # enter virtualenv
    $ workon [env_name]

### 1.2. Creating Your Project

Using this template to create a new Django app is easy::

    $ pip install django
    $ django-admin.py startproject --template=https://github.com/heroku/heroku-django-template/archive/master.zip --name=Procfile [project_name]
    $ cd [project_name]
    $ pip install -r requirements.txt

### 1.3. Run Local Server

    $ python manage.py migrate
    $ python manage.py runserver [port_number]

### 1.4. Deployment to Heroku

    $ git init
    $ git add -A
    $ git commit -m "Initial commit"

    $ heroku create [app_name]
    $ git push heroku master
    
    # If you encounter an error with DB
    $ heroku run python manage.py migrate

## Useful Heroku Commands

### 2.1. Create/Listing/Destroy App

    $ heroku crete [app_name]
    $ heroku list
    $ heroku destroy [app_name]

### 2.2. Access to App

    $ heroku run bash
    
### 2.3. Show Status/Log

    $ heroku ps
    $ heroku logs

See also, a [ready-made application](https://github.com/heroku/python-getting-started), ready to deploy.

## License: MIT

## Further Reading

- [Gunicorn](https://warehouse.python.org/project/gunicorn/)
- [WhiteNoise](https://warehouse.python.org/project/whitenoise/)
- [dj-database-url](https://warehouse.python.org/project/dj-database-url/)
