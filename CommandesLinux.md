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

  - ### Connexion en Super user ou un compte autre
```bash
  Su - (Compte root)
  Su - username
```
##### *Exit pour quitter l'user qu'on a emprunté*

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

- ### **Voir contenu supérieur doc txt**
```bash
head [OPTIONS] [FICHIER]
```
##### *option -n = choisir le nombre de ligne qu'on veut afficher*

- ### **Voir contenu inférieur doc txt**
```bash
tail [OPTIONS] [FICHIER]
```

- ### **Voir le contenu d'un document pour le modifier**
```bash
nano nomfichier
```

- ### **écrire nouvelle ligne sur un document**
```bash
echo "Message voulu" >> nomfichier
```

- ### **Filtrer recherche**
```bash
grep [OPTIONS] MOTIF [FICHIER]
```

- ### **Donner des droits à un fichier**
```bash
chmod [<SET><ACTION><PERMISSIONS>]... FICHIER
```
| Command | Description   |                        |                        |         |
| :---:   | :---:         |:---:                   | :---:                  | :---:   |
| Set     | U : User      | G : Group              | o : others             | a : all |
| action  | + : add droit | = : affecter le droit  | - : Supprimer le droit |         |
| perm    | r : read      | w : write              | x : execute            |         |

- ### **Modifié propriété fichier**
```bash
chown [OPTIONS] [PROPRIÉTAIRE] FICHIER
```
##### *exemple : sudo chown root hello.sh*

- ### **copier des fichiers ou des partitions entières au niveau du bit.**
```bash
dd if=/dev/zero of=/tmp/swapex bs=1M count=50
```
| Command                 | Description                         |                               |
| :---:                   | :---:                               | :---:                         |
| dd if=/dev/zero         | if=chemin d'entrée                  |                               |
| of=/tmp/swapex          | of=fichier de sortie à écrire       |                               |
| bs=1M                   | bs=Taille du fichier voulu en octect| M=Mega, K=kilo etc            |
| count=20                |count=nombre de ligne à lire         |                               |

- ### **éteindre le système en toute sécurité**
```bash
shutdown [OPTIONS] HEURE [MESSAGE]
```

- ### **Information config réseau**
```bash
ifconfig [OPTIONS]
```
##### *iwconfig :wireless*

- ### **Afficher les processus**
```bash
ps [OPTIONS]
```
 Description              | PID = Id processus                  |TTY = Nom du terminal où est en cours le processus |Time = temps utilisé du processeur | CMD = commande utilisé pour le démarrer |
| :---:                   | :---:                               | :---:                                             |:---:                              |:---:                                    |

- ### **Obtenir des paquets**
```bash
sudo apt-get update
```
- ### **Installer des paquets / màj**
```bash
sudo apt-get install [paquet]
```

- ### **Supprimer paquet**
```bash
apt-get remove [paquet]
```
```bash
apt-get purge [paquet]
```

- ### **Modifier mot de passe**
```bash
passwd [OPTIONS] [UTILISATEUR]
```

- ### **ajouter un utilisateur**
```bash
adduser nomutilisateur
```

- ### **ajouter un utilisateur en contrôlant les droits Root)**
```bash
useradd -d /home/alf2 -m -s /bin/bash -g stagiaire -G sudo -u 1002 alf2
```
| Command                 | Description                                                         |
| :---:                   | :---:                                                               |
| -d /home/alf2 -m        | Créer un utilisateur dans /home/alf 2 si pas de dossier -m          |
| -s /bin/bash            | -s affecter le droit de commande                                    |
| -g stagiaire            | -g = Premier groupe                                                 |
| -G sudo                 | -G = groupe secondaire                                              |
| -u 1002 alf2            | ajouter un ID à l'utilisateur                                       |

- ### **Supprimer un utilisateur**
```bash
deluser -r username 
```

- ### **modifier password**
```bash
passwd nomutilisateur
```

- ### **modifier groupe d'un utilisateur**
```bash
usermod -g (ou -G) [Options] nomuutilisateur
```

- ### **Forcer changement password puis verifier**
```bash
passwd -e nomutilisateur
cat /etc/shadow | grep nomutilisateur
```
