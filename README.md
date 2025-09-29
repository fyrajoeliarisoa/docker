`` 
docker run hello-world:Lancer le test d’installation
``


##image##


``
docker search nom_image: Rechercher une image
exemple:docker search ubuntu
``



``
docker pull nom_image: Télécharger une image
exemple: docker nginx
``



``
docker image ls`:Lister les images locales
``


``
docker rmi nom_image:Supprimer une image
par exemple: docker rmi nginux
donc l'image Nginx est supprimée localement
``


##conteneurs##




``
docker run image:Lancer un conteneur
exemple: docker run debian
``



``
docker run -it image /bin/bash:Lancer avec un shell interactif
par exemple:docker run -it debian
``

``
docker ps
Liste les conteneurs en cours d'exécution.
Exemple : docker ps
``

``
docker ps -a
Liste tous les conteneurs, y compris arrêtés.
Exemple : docker ps -a
``

``
docker start [conteneur]
Démarre un conteneur arrêté.
Exemple : docker start monconteneur
``

``
docker stop [conteneur]
Arrête un conteneur en fonctionnement.
Exemple : docker stop monconteneur
``
``
docker restart [conteneur]
Redémarre un conteneur en cours d'exécution ou arrêté.
Exemple : docker restart monconteneur
``


##Gestion des conteneurs##


``
docker stop web 
Stopper un conteneur


Exemple:

docker stop -t 20 web


docker stop web : arrêter proprement le conteneur nommé "web" avec délai d'attente par défaut.

docker stop -t 20 web : arrêter avec un délai personnalisé de 20 secondes.

docker stop container1 container2 : arrêter plusieurs conteneurs en même temps.


``

``

docker start web: Relancer un conteneur arrêté

Exemple:
docker start web


docker start web : redémarre le conteneur "web" en arrière-plan.

docker start --attach web : redémarre et affiche la sortie dans la console.

``



