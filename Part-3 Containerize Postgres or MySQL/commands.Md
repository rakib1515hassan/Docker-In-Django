## Part#1
    >> docker build --tag python-django .
    >> docker run --publish 8000:8000 python-django



Part#2
## It builds the image
    >> docker-compose build

    >> docker-compose run --rm app myproject startproject core .
    >> docker-compose up


## Part#3
    >> docker-compose build
    >> docker-compose run --rm app django-admin startproject core .

    >> docker-compose run --rm app python manage.py makemigrations
    >> docker-compose run --rm app python manage.py migrate
    >> docker-compose run --rm app python manage.py createsuperuser


    >> docker-compose up
    >> docker exec -it django_container /bin/bash