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




