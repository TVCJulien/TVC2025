  - ### Lister les processus 
  ```bash
  ps (Liste les processus lié à la console
  ps -aux (Listé tout les processus)
  ````
  - ### Surveillance temps réel des processus
  ```bash
  top
  ````

  - ### Tuer un processus
  ```bash
  kill -Signal "PID" (numéro)
  pkill nom (permet de tuer depuis le nom)
  kill -9 SignalPID (Force l'arrêt immédiat)
  ````

  - ### Liste processus en fonction de critères
  ```bash
  pgrep -u username
  pgrep -u cdurand
  ```

  - ### Afficher liste des processus en arrière plan avec un numéro
  ```bash
  Jobs
  ````
  - ### Afficher l'arborescence des processus
  ```bash
  ps -e -o pid,ppid,comm --forest
  ```

  - ### Voir la place disponible sur disk
  ```bash
  df
  ````

  - ### Voir la mémoire ram
  ```bash
  free (-h) permet d'afficher en Mega ou Giga
  ````

  - ### Afficher l'espace pris par un document/fichier en particulier
  ```bash
  du -sh /var/log
  ````

  - ### Pour ne pas vérouiller le fichier en mode écriture
  ```bash
  tail -n 5 dossier (-n 5 pour lister les 5 dernière ligne)
  taill 5 fonctionne aussi
  less marche auss
  ````
  - ### Pour Chercher les 100 dernières lignes avec une erreur
  ```bash
  tail -n 100 boot.log.2 | grep error
  ```

  - ### Afficher tout les logs systèmes (Du plus ancien au récent)
  ```bash
  journalctl
  ```

  - ### Afficher les logs d'un service qu'on veut (Du plus ancien au récent)
  ```bash
  journalctl -u nomservice
  ````

  - ### Afficher les logs d'un service qu'on veut (Du plus récent au plus ancien)
  ```bash
  journalctl -xeu nomservice
  ```

  - ### Afficher les logs jusqu'à une date/heure spécifié
  ```bash
  journalctl  --until <date>
  ```

  - ### Chercher les erreurs lié à un utilisateur
  ```bash
  journalctl -g SearchUser
  ```

 - ### Diagnostique Apache2 situation

##### Vérifier état service
```bash
systemctl status apache2
```

##### Si serv arrêté
```bash
systemctl start apache2
```

##### Vérifier état service
```bash
systemctl status apache2
```

##### Si besoin, inspecter log services
```bash
journalctl -xeu apache2
```

##### Fichier config dans /etc/default
```bash
cd /etc/default/
```
 
