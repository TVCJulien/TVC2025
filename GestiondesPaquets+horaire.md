afficher la list des sources apt 
```bash
cat /etc/apt/sources.lits
```


Mettre à jours la liste des paquets dispo
```bash
apt update
```
si ign = ignore = impossible à dl


Lancer la mise à jours des paquets
```bash
apt upgrade
```

pour lister et les mettres à jours
```bash
apt update && apt upgrade
```

Installer un paquets
```bash
apt install nomdupaquet
(si dispo dans la liste de base)
```

Voir la list des paquets installés 
```bash
dpkg -l
récuperer spécifiquement un nom dpkg -l | grep nomdupaquet
```

Installé un paquet qui n'a pas de distrib linux et dev qui ne ofurnis pas de dépots
```bash
Placez vous dans le répertoire /tmp.
Téléchargez discord avec la commande wget :
wget discord.deb "https://discord.com/api/download?platform=linux&format=deb

renommer le paquet récupérer
mv nomdufichier nouveaunom (possible de le trouver avec ls)

installer le paquet
dpkg -i discord.deb
```

Corriger les problèmes en cas de dépendances manquantes
```bash
apt --fix-broken install

supprimer paquet 

apt remove nomdupaquet laisse les fichiers de configuration
```

supprimer paquet 
```bash
apt purge nomdupaquet supprime même les fichiers de configurations
```

supprimer avec les dépendances
```bash
apt autoremove nomdupaquet (Si pas de nom de paquet supprime tout les paquets orphelins)
```

chercher si un paquet existe dans la bibliothéque de la distribution
```bash
apt search nomdupaquet
```

mettre à jours un paquet spécifique spécialement
```bash
apt install --only-upgrade nomdupaquet
```


ajouter des dépots extérieur à la librairie
```bash
cd/etc/apt/sources.list.d/
(enregistrer des dépots dedans)

Ce rendre dans /usr/share/keyrings/.
pour télécharger une fois dedans
wget lien du paquet
exemple :
wget https://dl.google.com/linux/linux_signing_key.pub

Pour renomer la key
mv NomKeygpctuelle nomVoulu
modifier format de la clé

Modifier format de la clé

gpg--dearmor google-key.pub > google-key.gpg
```

Mettre à jours complètement le système des distributions intallé
```bash
apt full-upgrade
si besoin de nettoyer cache
apt autoclean et suppression des paquets inutiles apt autoremove
```

Upgrade la distribution 
```bash
apt dist-upgrade
```

vérifier heure système
```bash
date
```

Voir si l'horloge est synchro
```bash
timedatectl timesync-status
```

Se synchro avec une Horloge internet
```bash
/etc/systemd/timesyncd.con
nano timesync.conf
mettre le serveur qu on souhaite à la ligne #NTP = lien (Ne pas oublier de retire le # qui est pour les commentaires)

Redémarrer le service pour actualliser
systemctl restart systemd-timesyncd.service
```

Recupérer la list des times zones possibles

```bash
timedatectl list-timezones
```
