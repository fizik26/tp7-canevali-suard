# Compte-rendu du TP07
## IRC 2018-2019 - Groupe 13
## Boot, processus, services
### Simon SUARD - Alexis CANEVALI
## GRUB
### Q1 à Q4
Dans le fichier grub, des options d'entête permettent de modifier les options de de démarrage.
On modifie `GRUB_TIMEOUT = 10`  pour définir à 10 secondes le temps d'attente de Grub
### Q5
Redémarrer la machine en maintenant shift pour accéder à Grub.
`vbeinfo` permet d'afficher différents paramètres pour reconnaître la dénition de l'écran.
"prefered-mode" affiche la définition recommandée pour l'écran.
Ensuite dans le fichier de configuration grub `GRUB_GFXMODE=definitionxdefinition`
Puis on on n'oublie de mettre à jour grub.
### Q6
Une fois le paquet téléchargé, il suffit de déplacer l'image dans `/boot/grub` et de faire un `grub-update`. Une confirmation par ligne de commande sera affichée.
### Q7 
Les thèmes sont installés dans `/boot/grub/themes`
On set ensuite le thème dans le fichier de conf `GRUB_THEME="/boot/grub/themes/ubuntu-mate/theme.txt`
### Q8
On modifie le fichier "/etc/grub.d/40_custom" 
Pour chaque nouvelle option qu'on veut ajouter, on fait:
`menuentry "nom option à afficher"{
   disque à démarrer ou commande à éxecuter
}`
### Q9

## Boot, processus, services
### Q1
`sudo apt install build-essential` permet d'installer tous les outils nécessaires à la compilation de programmes en C
### Q2
Création de hello.c
### Q3
Création du Makefile
### Q4
`make` puis `sudo make install` pour installer le module
### Q5
`modprobe -a hello.ko` permet de charger le module et on peut voir le message dans le journal du noyau grâce la commande `lsmod`
### Q6
`modinfo hello.ko` donne les informations tels que la version, la description, l'auteur et la license
### Q7
`modprobe -r hello.ko` permet de décharger le module et d'afficher le message dans le journal du noyau avec la commmande `lsmod`
### Q8
On ajoute au fichier /etc/modules la ligne hello.ko

## Interception de signaux
### Q1 & 2
La commande `exit` est exécutée
CTRL Z => SIGSTP
### Q3
CTRL C => SINGINT
 
