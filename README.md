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

#### apply those migrations to the database

`python manage.py migrate`

#### Return SQL of a migration

`python manage.py sqlmigrate appname 0001`

#### Check for problems in the project witthout running migrations

`python manage.py check`

#### Use django in shell

`python manage.py shell`

### API

#### [Related objects reference](https://docs.djangoproject.com/en/4.1/ref/models/relations/)

## Django Admin

### Creating an Admin user

#### `python manage.py createsuperuser`

#### Timezone

    change timezone to your current timezone using [timezone reference](https://docs.djangoproject.com/en/4.1/ref/settings/#std-setting-TIME_ZONE)

### Tests
#### Running tests
`python manage.py test appname`

### Testing a view
Use django test client to simulate a user interacting with the code at the view level. It can be used in the `test.py` or even in the view

#### Setting up the view test environment
[`from django.test.utils import setup_test_environment`
`setup_test_environment()`]
`setup_test_environment()` installs a template renderer which allows us to examine some additional attributes on responses such as context that would otherwise be unavailable. This method doesn't set up a test database.

##### Import the test client class
`from django.test import Client`
##### Create an instance of the client
`client=Client()`

##### Testing the view in shell
![Testing the view in shell](https://user-images.githubusercontent.com/83899148/215973204-b0fd8bc4-6db5-424f-937f-ad5abde17c27.png)

##### [Advanced Testing](https://docs.djangoproject.com/en/4.1/topics/testing/advanced/#topics-testing-code-coverage)

#### To access Django source files:
`python -c "import django; print(django.__path__)"`

#### [example tut](https://docs.djangoproject.com/en/4.1/intro/tutorial01/)

#### [Avoiding race conditions](https://docs.djangoproject.com/en/4.1/ref/models/expressions/#avoiding-race-conditions-us)

#### [installed apps](https://docs.djangoproject.com/en/4.1/ref/settings/#std-setting-INSTALLED_APPS)

#### [Django admin documentation](https://docs.djangoproject.com/en/4.1/ref/django-admin/)

#### [Django url dispatcher](https://docs.djangoproject.com/en/4.1/topics/http/urls/)

#### [Django generic views](https://docs.djangoproject.com/en/4.1/ref/class-based-views/generic-display/#django.views.generic.list.ListView)
