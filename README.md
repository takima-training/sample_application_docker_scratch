Vous avez fait votre première connection à Travis et SonarCloud, bien joué !

Nouvelle étape, vous avez différents services qui fonctionnent (httpd, simple-api, database).
Essayer de les lancer sur votre machine via le `docker-compose.yml` présent.
Tout doit fonctionner.

L'idée va être de construire chaque image, de l'envoyer sur Docker Hub 
puis de déployer les changements sur le serveur distance.

Pour commencer ajouter les fichiers à votre dépôt Git et faîte une nouvelle CI
qui va :

1. Build chaque image et la push sur DockerHub (une étape par service)
2. Utiliser Ansible pour faire les éléménts suivants depuis votre CI sur votre serveur :
	- Installer Docker
	- Installer docker-compose
	- ouvrir le port spécifique (80)
	- installer le dernier `docker-compose.yaml`
	- relancer le docker-compose
