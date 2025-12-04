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

supprimer paquet 
```bash
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

pour renomer la key
"mv NomKeygpctuelle nomVoulu
modifier format de la clé

Modifier format de la clé

gpg--dearmor google-key.pub > google-key.gpg
```


