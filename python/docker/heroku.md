## debug logs in heroku
    heroku logs --tail --app her-sadig
## to push changes to heroku
    git push heroku master
## list all tracked git files
    git ls-tree -r master
## run migrations in heroku container
    heroku run python manage.py migrate -a her-sadig
## bash commands in heroku container
    heroku run ls /app --app her-sadig
## log inti heroku container
    heroku run sh --app her-sadig
    