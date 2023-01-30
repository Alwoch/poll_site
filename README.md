# Getting started:

### Creating a virtual environment
  `python -m venv envname`
### installing django
  `python -m pip install django`
### starting a django project
  `django-admin startproject myproject`
### starting the development server
   `python manage.py runserver`
### running the project on a specific port
   `python manage.py runserver 8080`
### creating a django app
   The app should be created in the same folder as the manage.py so that it is imported as its own top level module rather than a submodule of the project
   `python manage.py startapp appname`

## settings.py
#### setting up databases
    [database documentation link](https://docs.djangoproject.com/en/4.1/ref/settings/#std-setting-DATABASES)
#### Add an app to the installed apps
   Add an object path to the installed Apps array in the settings.py like `polls.apps.PollsConfig`
#### Make migrations for new changes in an app
   `python manage.py makemigrations appname`
##### apply those migrations to the database
   `python manage.py migrate`
#### Return SQL of a migration
   `python manage.py sqlmigrate appname 0001`
#### Check for problems in the project witthout running migrations
   `python manage.py check`
#### Use django in shell
   `python manage.py shell`
   



#### Timezone
    change timezone to your current timezone using [timezone reference](https://docs.djangoproject.com/en/4.1/ref/settings/#std-setting-TIME_ZONE)
#### [installed apps](https://docs.djangoproject.com/en/4.1/ref/settings/#std-setting-INSTALLED_APPS)

#### [Django admin documentation](https://docs.djangoproject.com/en/4.1/ref/django-admin/)

