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

19- Créer un Token pour les utilisateurs
    inclure dans settings.py 'rest_framework.authtoken' puis faire python manage.py migrate

20- dans l'admin en ligne, créer le token pour notre super user

21- dans urls.py de notre repertoire movierater
    ajouter l'url auth puis importer obtain_auth_token pour obtenir le token du super user
    dans POSTMAN, http://127.0.0.1:8000/auth/, method POST
    renseigner le username et le mot de passe du super user
22- proteger une route par le token
    dans views.py, ajouter authentication_classes = (TokenAuthentication, ) dans la class MovieViewSet
    pour proteger les movies

23- renseigner le token dans les routes pour avoir l'autorisation de les utiliser
    exemple: dans POSTMAN, pour obtenir les movies
    dans le header, ajouter Authorization - Token suivi du token

24- Enregister un utilisateur
    créer la class UserViewSet dans views.py puis la configurer
    créer UserSerializer dans serializers.py
    dans urls.pi du repertoire api, enregistrer le UserViewSet

25- créer un utilisateur dans POSTMAN