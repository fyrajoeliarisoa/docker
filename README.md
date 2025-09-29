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


``
docker rm -f web :Supprimer un conteneur


Exemple:

docker rm -f web

La commande docker rm sert à supprimer un conteneur qui est arrêté.

L'option -f (force) arrête le conteneur s'il est en cours d'exécution, puis le supprime immédiatement.

Une fois supprimé, le conteneur ne peut plus être redémarré, sauf à recréer un nouveau conteneur à partir de l'image Docker.

``


##Variables d’environnement##

``

docker run -tid --name test --env MYVAR=123 ubuntu
docker exec -ti test env : Vérifier la variable dans le conteneur

Exemple:
docker run -tid --name test --env MYVAR=123 ubuntu
-t : alloue un pseudo-terminal

-i : garde l'entrée standard ouverte

-d : lance le conteneur en arrière-plan (détaché)

--name test : nomme le conteneur "test"

--env MYVAR=123 : définit la variable d'environnement MYVAR avec la valeur 123

ubuntu : image utilisée (version standard Ubuntu)
``


##Nettoyage rapide##

``

docker rm -f $(docker ps -aq)      # Supprimer tous les conteneurs
docker rmi -f $(docker images -q)  # Supprimer toutes les images

Exemple
docker rm -f $(docker ps -aq)

docker ps -aq liste tous les conteneurs, actifs et inactifs, en ne retournant que leurs IDs.

docker rm -f force la suppression de ces conteneurs, les arrêtant si nécessaire avant de les supprimer


``


##Volumes##


``
Création de volume simple:
docker volume create mynginx
docker volume ls
``

``
un volume avec un conteneur
docker run -itd -p 8080:80 -v mynginx:/usr/share/nginx/html --name c1 nginx

``

``
Inspecter un volume :
docker volume inspect mynginx

``




