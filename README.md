# Linux


**TP challenges**
---

TD 1: Chapitre 1, Installation et Utilisation

**Le premier:**

Le fichier /etc/passwd défini les utilisateurs, le 4ieme champ contien l'id de groupe le gid.
Trouvez, en une seule ligne de commande utilisant des filtres combinés, quel est le gid le plus utilisé.

Réponse: `id -g sync`


**Le deuz':**

Le fichier /etc/group defini les groupes connu du système
dans une ligne de commande on peu substitué une partie de la ligne de commande par le résultat d'une ligne commande $(commande)

Exemple:
        `echo mon uid est $(grep alan /etc/passwd | cut -d: -f3 | head -1)`
        
En utilisant ceci et la réponse à la première question, affichez en une seule commande le nom du groupe associé au gid le plus utilisé

Réponse: `echo mon uid est $(grep bianco /etc/passwd | cut -d: -f3 | head -1)`



## Other TD 2

**Variable Shell**


Variables

Créez une variable rototo et assignez lui la valeur "Blurps"

Affichez la valeur de la variable rototo

Affichez les valeurs courantes associées aux variables :

LOGNAME
COLUMNS
LINES


Redimentionez votre fenêtre terminal et réaffichez les valeurs de COLUMNS et LINES


Export
Vous allez ajouter à votre installation ubuntu la langue française et les pages du man en français.

`$ sudo apt-get install language-pack-fr manpages-fr`

Consultez le man, il est toujours en anglais.
La langue française et le man en français sont bien installés mais pas utilisés.
Dans votre terminal, exportez la variable LANG avec la valeur "fr_FR.UTF-8"

`$ export LANG=fr_FR.UTF-8`

Consultez le man de nouveau. La variable LANG exportée est maintenant utilisée par la commande man afin de chercher la page de manuel en français.

PATH
Lancez un sous shell :

`$ bash`
Votre shell à donc lancé un second shell bash ; vous êtes maintenant dans une nouvelle session shell.

Affichez votre PATH :

`$ echo $PATH`
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

Videz la variable PATH
`$ PATH=""`

Essayez une commande puis quittez le second shell :
`$ ls fichier.txt
$ /bin/ls fichier.txt
fichier.txt
bash: ls: No such file or directory
$ exit
Le shell ne retrouve plus la commande /bin/ls si on ne précise pas son chemin. Après avoir quitté le second shell votre variable PATH est retrouvée.`

Alias
--
listez les alias définis ? 
Réponse: `Alias`

lesquels sont remarquables selon vous ?
Réponse: `ls -al` ou `ll`

Configuration
Mettez en place ce qu'il faut pour avoir un pompte et une complétions adapté à une utilisation intensive de git.

Réponse: `echo $PS1`
         `PS1=""`

