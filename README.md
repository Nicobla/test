# Bienvenue sur le serveur de mini-jeux en GoLang !

## Langages utilisés

+ GoLang, Python, C++
+ HTML5, CSS3, JavaScript, jQuery

## Configurer le serveur

Pour modifier les paramètres du serveur, ouvrez le fichier *config/server.json* et modifiez le/les paramètres qui vous intéressent:
1. ```LogLevel``` niveau de log
	+ ```release``` affiche uniquement les messages de démarrage et d'extinction du serveur
	+ ```error``` affiche les erreurs
	+ ```debug``` affiche tout le détail des fonctions)
2. ```LogPath``` chemin du dossier des fichiers de logs (pas d'enregistrement si nul)
3. **```TCPAddr```** adresse IP et port du serveur (port par défaut: 3563)
4. **```WSAddr```** adresse IP et port du serveur (port par défaut: 3653)


## Configurer le client web

Pour modifier l'adresse de connexion au serveur du client web, ouvrez le fichier *ClientsWeb/ressources/main.js* et éditez la ligne suivante au début du fichier:
```
ip = "127.0.0.1", port = "3653"
```

## Installation du robot Python

Pour lancer le robot Python, il faut au préalable installer plusieurs modules :
```
python -m pip install websockets
		      websocket
		      numpy
		      websocket-client
```

## Commandes du robot Python

Pour lancer le bot Python, il faut se placer dans le répertoire du robot (ClientsRobots/Python/), et écrire la commande:
```python BotPython.py```

À cette commande, vous pouvez ajouter des paramètres de lancement, parmis les suivants:

+ ```-h, -help```			Affiche le manuel de commande
+ ```-g, -game [morpion/puissance4]```	Définit le jeu sur lequel le bot joue (morpion ou puissance4)
+ ```-s, -serveur [IP]```		Définit l'adresse IP de connexion au serveur
+ ```-p, -port [port]```		Définit le port de connexion au serveur
+ ```-n [pseudo]```			Définit le pseudo du bot
+ ```-l, -log [error/warning/debug]```	Définit le niveau de log (Error, Warning ou Debug)


## Liste de commandes de lancement du bot C++

_*vide*_













## Lien test
[https://github.com/becodeorg/BXLAnderlecht/blob/master/08-AJAX/php-chat.md](https://github.com/becodeorg/BXLAnderlecht/blob/master/08-AJAX/php-chat.md)

## Screenshots 

Tout _**pleins**_ de fonctionnalités qui arriveront d'ici peu! Les conversations privées, les smileys, la possibilité de gérer son statut, ... 

![Connexion](https://i.imgur.com/BxP73v9.png)
