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
