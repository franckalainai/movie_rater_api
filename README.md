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
7- inserer api et rest_framework dans notre ficher settings.py
    'rest_framework',
    'api',
8- python manage.py migrate
9- créer le super user
    python manage.py createsuperuser
10- creation de nos models movie et rating
11- migrations de nos models
    python manage.py makemigrations
    python manage.py migrate
12- Enregistrer les models movie et rating dans admin.py
13- creer le fichier serializers.py et le configurer pour afficher nos models dans l'api
14- configurer views.py pour le serializer
15- Enregistrer les urls dans api/urls.py
16- Personnaliser les methodes create et update pour rating dans views.py
17- obtenir le nombre de rating pour un movie
    creer un fonction no_of_ratings() dans la class Movie de models.py pour obtenir le nombre de rating
    inclure la fonciton dans la class MovieSerializer dans serializers.py
18- obtenir la moyenne des ratings
    creer une fonction avg_rating() dans la class Movie de models.py 
    inclure la fonction dans MovieSerializer dans serializers.py
