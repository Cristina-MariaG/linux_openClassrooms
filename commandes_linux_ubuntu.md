
ls
cd 

cat -consulter un fichier

cat fichier or cat /fichier1 / fichier 2
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
