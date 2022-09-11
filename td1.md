# Exercice 2

## Manuel
1.	Which permet de localiser une commande, une binaire
2.	Pour chercher un terme dans une page du manuel, il faut écrire le terme précédé par un `/`, puis naviguer à l’aide de la lettre `n` ou `N`, pour aller au terme suivant ou précédent.
3.	On peut quitter le manuel avec la touche `q`
4.	La section 6 parle des jeux et petits programmes ludiques disponibles sur le système

## Navigation dans l’arborescence des fichiers
1.	Pour aller dans le dossier `/var/log`, il faut écrire comme commande `cd /var/log`
2.	Pour remonter dans le dossier parent par un chemin relatif, il faut utiliser la commande `cd ..`
3.	Pour retourner dans le dossier personnel, utiliser la commande `cd`
4.	Pour revenir au chemin précédent sans écrire de chemin, utiliser la commande `cd –`
5.	Je ne possède pas la permission d’accéder au dossier `root`
6.	Cela ne fonctionne car `sudo` ne peut fonctionner qu’avec des executables, or `cd` est un shell builtin, et donc n'a pas de Path
7.	On crée les dossiers avec la commande `mkdir`, puis on crée les fichier en se mettant dans chacun des dossiers, puis la commande `touch`
8.	Le fichier1 est bien supprimé avec `rm`, cependant le dossier n’est pas supprimé car il s’agit d’un dossier et non d’un fichier
9.	La commande pour supprimer un dossier est `rmdir`
10.	On ne peut pas car le dossier n’est pas vide
11.	On peut supprimer un dossier non vide avec `rm –rf`

## Commandes importantes
1.	Pour afficher l’heure, il faut utiliser la commande `date`, la commande `time` chronomètre ou évalue les ressources employées par une commande simple
2.	Les fichiers commençants par un point ne sont pas affichés lorsque l’on utilise la commande `ls`
3.  En utilisant la commande `which`, on sait que ls se situe dans `/usr/bin/ls`
4.  Il n'existe pas d'entrée de manuel pour la commande `ll` car il s'agit d'un alias pour `ls -alF`
5.  Pour afficher tous les dossiers de bin, il faut taper `ls /bin`
6.  La commande `ls ..` permet d'afficher la liste des fichiers du dossier parent
7.  Pour obtenir le chemin complet du dossier courant, utiliser la commande `pwd`
8.  Cela crée le fichier plop une fois car la seconde itération de `echo 'bip' > plop` remplace la première, il n'y a donc qu'un seul bip
9.  `echo 'bip' >> plop` cependant écrit au sein du fichier plop à nouveau bip, et ce en dessous de la première itération
10.  La commande `echo 'toto'`écrit juste toto, cependant la commande `sleep 10` suspend l'éxecution d'une nouvelle commande durant 10 secondes
11.  La commande `file` permet de connaître le type de fichier 
12.  Le fichier lien_phy a récupéré la modification d'original, cependant en supprimant original lien_phy ne disparait pas
13.  Les deux fichiers peuvent se modifier entre eux, cependant la suppression de lien_phy entraîne la suppression du contenu de lien_sym
14.  POur stopper le défilement de syslog il faut utiliser les raccourcis crtl+s et ctrl+q
15.  Pour afficher les 5 première lignes, il faut taper `head -5 syslog`, pour les 15 dernières `tail -15 syslog`, et les lignes de 10 à 20 `gead -10 syslog | tail n+5`
16.  La commande `dmesg`affiche tous les messages, et `less`les affiche en terme de page
17.  Le fichier `etc/passwd` regroupe une base de données textuelle d'informations sur les utilisateurs qui peuvent se connecter au système. La commande pour afficher dans le manuel est `man 5 passwd`
18.  Pour afficher la première colonne dans le sens inverse, il faut taper `cat passwd | awk '{ print$1 }' | sort -r`
19.  Pour compter le nombre d'utilisateurs, il faut taper `who | wc -l`
20.  Pour compter le nombre de pages de manuel avec le mot conversion, il faut écrire `man -k conversion | wc -l`
21.  Il faut taper `find -name passwd`
22.  
