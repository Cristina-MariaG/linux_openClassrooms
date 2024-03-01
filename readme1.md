# Linux

## Terminal/ Shell/ Prompt

$echo $SHELL --to know the shell type

ls
ls  -l (avec details) or -l -t (modifié plus recemment)
ls -l -r (les plus vieux elem en premier)
ls -l -t -r = ls -lrt

ls -lRt = plus details s'il y a des dossier avec des fichiers trouvé dans notre dossier ou on fait ls

ls -lRth = volume des fichiers traduit en oct or mb

ls -lrth rep1 liste que le repertoire 1 
lrt - options et rep1 est argument

ls -lrtha

affiche les fichiers cachés

il y a des commandes buitin et des commandes externe (present comme un fichier)
type echo --return echo is a shell builtin
type bash =bash is /usr/bin/bash 

file /usr/bin/bash --infos sur le fichier

 file /../* touts les fichiers
 
 cd /home/.../ && file * ---double commande
 echo un && echo deux

 id --command pour info sur l utilisateur 
type id  = comand extern presente dans un fichiere

echo $PATH

( id est executable car la commande se trouve definie dans un repertoire de path)

on peut ajouter des fichier a path pour pouvoir les executer de partout comme id comme ça: (repertoirie referencé dans la var path)
export PATH=$PATH:/adresse des fichiers qu on veut pouvoir executer de partout/ 
on verifie echo $PATH qui doit contenir l adresse just ajouté


help =liste des commandes interne dispo dan sle shell

help echo = details sur echo commande interne

commande externe( exp id) : commande --help

id --help = resumé
man (manuel) 
man id = plus detaillé


history

pour une commande de history:
!number qui se trouve apres ce qu'on tappe history


ctrl +r = recherche de commande avec une partie tappé
de nouveau ctrl+r pour remonter dans l'historique

#aliase
type ls = aliase...

pour ajouter des aliases on doit modifier le fichier .bashrc et ajouter 
![alt text](image-1.png)
declaration d alias:
ajouter dans .bashsrc
alias ll='ls -lrtha'
