[django](https://docs.djangoproject.com/en/2.2/intro/tutorial03/)  
## to start application 
    python manage.py startapp polls
## in polls/view.py  add 
    from django.http import HttpResponse
    
    
    def index(request):
        return HttpResponse("Hello, world. You're at the polls index.")
## in polls/urls.py
    from django.urls import path
    
    from . import views
    
    urlpatterns = [
        path('', views.index, name='index'),
    ]        
## add 'polls.apps.PollsConfig',   to settings.py file to add app in project        
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
 
## define __str__ method  
        def __str__(self):
            return self.question_text
##  list all objects
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
## register object in models.py (database table )  in admin.py file
    from django.contrib import admin
    
    from .models import Question
    
    admin.site.register(Question)   
    
      
        