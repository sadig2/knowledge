[django](https://docs.djangoproject.com/en/2.2/intro/tutorial03/)  
[rest api](https://scotch.io/tutorials/build-a-rest-api-with-django-a-test-driven-approach-part-2)
[django mail](https://wsvincent.com/django-contact-form/)
[django-cms](http://docs.django-cms.org/en/latest/index.html)
[django-rest-framework](https://github.com/encode/django-rest-framework/tree/master/rest_framework)

## to create virtual environment for python2

    virtualenv venv --python=python2.7

## to create virtual environment

## install python3
    sudo apt-get install python3.9-venv

    sudo apt install -y python3-venv
    python3 -m venv venv1

## update pip

    pip install --upgrade pip
    pip install --upgrade django
    pip install --upgrade setuptools

## to install django and django-admin

    pip install django django-admin

## to create project

    django-admin startproject name

## to start application

    python manage.py startapp polls
    django-admin startapp quickstart

## in polls/view.py add

    from django.http import HttpResponse


    def index(request):
        return HttpResponse("Hello, world. You're at the polls index.")

## to save necessary dependencies of django project that i installed for future development

    pip freeze > requirements.txt

## to read from saved file to install deeded dependencies

    pip install -r requirements.txt

## in polls/urls.py

    from django.urls import path

    from . import views

    urlpatterns = [
        path('', views.index, name='index'),
    ]

## add 'polls.apps.PollsConfig', to settings.py file to add app in project

## to see sql commands run

    python manage.py sqlmigrate polls 0001

## to activate django shell

    python manage.py shell

## import Question class from models.py

     from polls.models import Question

## create object of Question class

    q = Question(question_text="What's new?", pub_date=timezone.now())

## import timezone , Question

    from polls.models  import Question
    from django.utils import timezone
    a = Question(var1 = "" , var2 =  " " )
    a.save()
    a.var1   - will show first variable

## define **str** method

        def __str__(self):
            return self.question_text

## list all objects

    Question.objects.all()

## django keyword lookup

    Question.objects.filter(id=1)
    Question.objects.filter(question_text__startswith='What')

## custom method

    q = Question.objects.get(pk=1)   - get object at first index
    q.waspublishedrecently

## create user for admin page

    python manage.py createsuperuser

## run test server

    python manage.py runserver

## runserver with multiple settings files

    python manage.py runserver --settings=mysite.settings.development

## register object in models.py (database table ) in admin.py file

    from django.contrib import admin

    from .models import Question

    admin.site.register(Question)

## django wagtail cms

[wagtail](https://www.dothedev.com/blog/integrate-wagtail-into-existing-django-project-django-blog-app/#)
