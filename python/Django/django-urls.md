## set up app.urls.py file 
    from django.urls import path
    
    from . import views
    
    urlpatterns = [
        path('', views.index, name='index'),
        # ex: /polls/5/
        path('<int:question_id>/', views.detail, name='detail'),
        # ex: /polls/5/results/
        path('<int:question_id>/results/', views.results, name='results'),
        # ex: /polls/5/vote/
        path('<int:question_id>/vote/', views.vote, name='vote'),
    ]
## methods in view.py to run when urls py invokes them
      from django.shortcuts import render
      
      # Create your views here.
      from django.http import HttpResponse
      
      
      def index(request):
          return HttpResponse("Hello, world. You're at the polls index.")
      
      def detail(request, question_id):
          return HttpResponse("You're looking at question %s." % question_id)
      
      def results(request, question_id):
          response = "You're looking at the results of question %s."
          return HttpResponse(response % question_id)
      
      def vote(request, question_id):
          return HttpResponse("You're voting on question %s." % question_id)

##   to match number in http request like localhost/43/
    <int:question_id>   i can name quaetion_id whatever i want
     