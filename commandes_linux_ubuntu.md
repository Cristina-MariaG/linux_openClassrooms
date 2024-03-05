
ls

ls -li (i = inode) (inode = nr avant les droits du fichier)



cd 

cp (copy)

cp fichier newnamefichier 


mv (move)

mv fichier newnamefichier 

ln (lien)

ln fichiersource fichierdestinzation ( destination garde le m^me nr de refference que la source)
mais si je modifie un de deux, quand je fais cat de l autre je vais avoir les même modif car la reference est la même donc a cette adresse de memire j'ai les modif 

cat fichier 1 > fichier2 (cree fichier 2 s il n existe pas et dit que fichier 1 pointe vers fichier 2)

ln -s (symbolique)

rm fichier


cat -consulter un fichier

cat fichier or cat /fichier1 /fichier 2
cat -n /fichier = avec nr de ligne

less - visualiser des fichiers
    - affiche une seule page a la fois
    - pour passer a la page suivante on tape espace
    - b pour revenir sur une page precedente
    - G -fin de fichier
    - g debut du fichier
    - avec "-N" on affiche des nr des lignes 
    - apres  -N on tappre 50 et g et on va a la ligne 50
    - /text -chercher text


grep -  permet de filtrer le flux de données selon un motif (pattern en anglais) passé en paramètre

grep mot_cherché /fichier

grep -n mot /fichier
grep -i mot /fichier pas case sensitive
grep -ni mot /fichier (i = pas case sensitive)
grep -nio mot /fichier ( afficher que le mot cherche dans le fichier et pas le reste du texte sur la ligne)

grep -rnio motCherche /fichier/* - cherche et affichie les resultats dans toute l'arborescence de /fichier

sed / awk


sed :

sed 's/Mot/MOT/'  /fichier : remplace Mot avec MOT dans fichier mais seulement pour lecture

or pour remplacer tous les mots soit avec majouscule soit minuscule mais seulement pour lecture (n 'enregistre pas):

sed 's/[M|m]ot/MOT/' /etc/os-release remplace les mots mot et Mot par MOT
sed 's/[M|m]ot/MOT/' /etc/os-release > /home/seb/os-release

pour enregistrer des remplacements

cat /etc/os-release >home/seb/os-release
sed -i 's/[M|m]ot/MOT/' /home/seb/os-release va changer les mots et enregistrer

sed -n 2,6p /fichier (p comme print, sorte standard)
sed -n 2,6p /fichier > /fichier

sort et cut

grep noologin /etc/password = cat /etc/password | grep nologin

| des pipes
cat /etc/password | grep nologin | grep -E "[0-9][0-9]" (no login  avec l id sup a 10)

cat /etc/password | grep nologin | grep -E "[0-9][0-9]" | sort (fais un  sort alphabetique)
cat /etc/password | grep nologin | grep -E "[0-9][0-9]" | sort | cut  -d :-f 1 (recuper le premier champ)
cat /etc/password | grep nologin | grep -E "[0-9][0-9]" | sort | cut  -d : f 1 | sed 's/games/seb/'  remplacer games par seb



chmod 

chmod u+rwx
chmod ugo-rw+x 
chmod 666= droits rw a tous
chmod 665= droits rw a user et groupe et droits rx aux autres
7 toutes les doits 
6 droits rw
5 rx
4 r
3 wx
2 w
1 x
0 - 

ls -l : L'ordre : rwx u, rwx g, rwx o

chown changer owner d un fichier

chown nomDeNouveauOwner:nomProprietaire fichierNom
il faut etre root pour pouvoir faire ce grenre de changelent

chgrp nomNouveauGroupeProprietaire proprietaire
chmod -R propt:propr * (donne toutes les droits sur tous les fichiers a seb) -R change même a l interieur des dossiers les droits sur ces fichiers de l'interieur


passwd permet de changer le mdp

SETUID bit droit

le droit rwsr... dit que tous herite des droits du compte proprietaire de la commande  setuid bit, 
pour attribbuer le role s: 
chmod 4755 fichier = rws sur le fichier
l attribution d un droit comme ça a un fichier donne le doits a tt le monde d executer le fichier 1 en se faisant passer par le proprietaire du fichier

Sticky Bit
chmod 1reste de bits fichier : 1744 par exmp donne les droits rwxr--r-T ou T represente Sticky bit : ts peuvent partager/modifier le fichier mais pas le supprimer