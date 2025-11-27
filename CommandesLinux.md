# **Rappel des commandes Linux**
  - ### Ouvrir un terminal
```bash
ctrl + alt + t
````

  - ### Lister le contenu d'un répertoire
```bash
  ls -l
```
##### *Possible ajout d'une option aprés -l (exemple ls -l /)*

- ### Naviguer dans les répertoires
```bash
cd
```
- ### Retour au répertoire parent
```bash
cd ..
```

- ### Naviguer sur un répertoire du dossier parent
```bash
cd ../NomRépertoire
```

- ### Afficher le chemin du répertoire
```bash
pwd
```

- ### Ouvrir l'aide pour une commande
```bash
man
```
##### *example: man ls*

- ### Créer un répertoire
```bash
mkdir ~/Dossier_Test
```

- ### **Supprimer un fichier/répertoire**
```bash
rm -r nomfichier
```

- ### **Bouger un fichier**
```bash
mv source destination/
```

- ### **Historique des commandes**
```bash
history
```

- ### **Retrouver un dossier**
```bash
find -name nom
```

- ### **Copier un fichier dans une source**
```bash
cp Source Destination
```
##### Pour copier l'entièreté du dossier Cp -r Source Destination

- ### **Créer un document .txt**
```bash
touch nomfichier
```

- ### **Voir contenu d'un document txt**
```bash
cat nomfichier
```

- ### **Voir le contenu d'un document pour le modifier**
```bash
nano nomfichier
```

- ### **écrire nouvelle ligne sur un document**
```bash
echo "Message voulu" >> nomfichier
```
