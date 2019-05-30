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
 
 
 
    