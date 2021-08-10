# movie_rater_api
1- creation du repertoire global du projet (movie_rater_api)
2- créetion de l'environnement venv
    python -m venv venv
    source venv/Scripts/activate
3- installer django rest framework
    pip install djangorestframework
4- creer le projet
    django-admin startproject movierater .
5- creer l'application du projet
    django-admin startapp api
6- notre premiere migration
    python manage.py migrate