# Bienvenue sur le serveur de mini-jeux en GoLang !

## Langages utilisés

+ GoLang, Python, C++
+ HTML5, CSS3, JavaScript, jQuery

## Compiler le serveur

Avant de compiler le serveur, assurez-vous d'avoir le compilateur GoLang installé, et que la variable d'environnement ```GOPATH``` soit correctement configurée (se référer à la documentation de GoLang)

## Lancer le serveur

+ Windows: Ouvrer le fichier Gameserver.exe
+ Linux: Exécuter le fichier Gameserver

Au lancement du serveur, s'il n'existe pas de fichier de configuration (cf. Configurer le serveur), le serveur va en créer un avec des variables par défaut.

## Configurer le serveur

Pour modifier les paramètres du serveur, ouvrez le fichier [*config/server.json*](config/server.json) et modifiez le(s) paramètre(s) qui vous intéresse(nt):

- ```LogLevel``` niveau de log
	+ ```release``` affiche uniquement les messages de démarrage et d'extinction du serveur
	+ ```error``` affiche les erreurs
	+ ```debug``` affiche tout le détail des fonctions)
- ```LogPath``` chemin du dossier des fichiers de logs (pas d'enregistrement si nul)
- ```TCPAddr``` adresse IP et port du serveur (port par défaut: 3563)
- ```WSAddr``` adresse IP et port du serveur (port par défaut: 3653)
- ```MaxConnNum``` maximum d'utilisateurs connectés en même temps autorisé
- ```TournamentMode``` mode de match-making
	+ ```true``` activé
	+ ```false``` désactivé
- ```NbGames``` nom de parties maximales que deux mêmes adversaires peuvent faire l'un contre l'autre **(si mode match-making activé)**
- ```TimeOut``` temps disponible à un joueur pour jouer son tour (en secondes)
- ```UniqueLogin``` deux joueurs ne peuvent pas prendre le même pseudo
	+ ```true``` activé
	+ ```false``` désactivé
- ```FirstToPlay``` détermine le joueur qui commence à jouer
	+ ```Random``` aléatoire
	+ ```AlternateFirstRandom``` aléatoire puis alterné
	+ ```FirstConnected``` premier connecté
- ```CaracteresInterdits``` caractères interdits pour les pseudos (["\\","/", "\"", "{", "}"] par défaut pour éviter les bugs du bot C++)
- ```WritesScoresAtClosure``` permet de choisir le moment d'écriture des fichiers excels
	+ ```true``` à la fermeture du serveur
	+ ```false``` au fur et à mesure

## Configurer le client web

Pour modifier l'adresse de connexion au serveur du client web, ouvrez le fichier [*ClientsWeb/ressources/main.js*](ClientsWeb/ressources/main.js) et éditez la ligne suivante au début du fichier:
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

Pour lancer le robot Python, il faut se placer dans le répertoire du robot [*ClientsRobots/Python/*](ClientsRobots/Python/), et écrire la commande:
```python BotPython.py```

À cette commande, vous pouvez ajouter des paramètres de lancement, parmis les suivants:

+ ```-h, -help```			Affiche le manuel de commande
+ ```-g, -game [morpion/puissance4]```	Définit le jeu sur lequel le robot joue (morpion ou puissance4)
+ ```-s, -serveur [IP]```		Définit l'adresse IP de connexion au serveur
+ ```-p, -port [port]```		Définit le port de connexion au serveur
+ ```-n [pseudo]```			Définit le pseudo du robot
+ ```-l, -log [error/warning/debug]```	Définit le niveau de log (Error, Warning ou Debug)


## Commandes de lancement du bot C++

Pour lancer le robot C++, il faut d'abord se placer dans le répertoire du robot [*ClientsRobots/C++/*](ClientsRobots/C++/)
	+ Windows: et ouvrir l'exécutable
	+ Linux: et ouvrir le fichier .sh
Il se lancera alors avec des paramètres par défauts.

Vous pouvez aussi le lancer avec une commande. À cette commande, vous pouvez ajouter des paramètres de lancement, parmis les suivants:

+ ```-h, --help```			Affiche le manuel de commande
+ ```-g, --game [morpion/puissance4]```	Définit le jeu sur lequel le bot joue (morpion ou puissance4)
+ ```-s, --serveur [IP]```		Définit l'adresse IP de connexion au serveur
+ ```-p, --port [port]```		Définit le port de connexion au serveur
+ ```-l, --log [error/warning/debug]```	Définit le niveau de log (Error, Warning ou Debug)
