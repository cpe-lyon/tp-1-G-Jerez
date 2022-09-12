# TP 1 : Admin Linux

**Exercice 2:**  
<ins>Manuel</ins>
1. Le rôle de la commande *which* est de donner le PATH d'un fichier.
2. Dans le `man which` on peut utiliser `/option` pour chercher option dans le `man which`.
3. On peut quitter le manuel en appuyant sur `q`.
4. La section parle de l'intro de la section (nom, description, notes, colophon).  
  
  <ins>Navigaton dans l'arborescence des fichiers</ins>  
1. Pour aller dans le dossier `/var/log/` on peut utiliser `cd /var/log/`.  
2. Pour remonter on peut utiliser `cd ..`.
3. Pour ce faire il faut exécuter `cd ~`.
4. Pour retourner dans le dossier précédent sans utiliser de chemin relatif on peut utiliser `cd -`.
5. La permission d'acccès au fichier `/root/` nous est refusée.
6. La commande ne peut s'executer car elle est builtin shell et n'existe pas nativement dis le retour d'erreur. Cela se produit car sudo ne fonctionne que sur des executables et cd n'est pas un executable mais est un builtin de bash.
7. On peut créer les dossier à l'aide de la commande `mkdir [dirname]` `touch [filename]`.
8. A l'aide de `rm` on peut supprimer `Fichier1` mais pas `Dossier1` car il s'agit d'un dossier et non d'un fichier.
9. Il faut utiliser `rmdir` pour un dossier.
10. Quand on applique cette commande au `Dossier2`, elle ne s'execute pas car le `Dossier2` n'est pas vide.
11. On peut supprimer le `Dossier2` et tout son contenu à l'aide de `rm -rf Dossier2`.
  
  <ins>Commandes importantes</ins>
  1. La commande permettant d'afficher l'heure est `date` et pour plus de précision et avoir uniquement l'heure minute seconde il faut utiliser `date | awk '{print $4}'`. La commande `time` execute des programmes et affiche l'utilisation des ressources systèmes.
  2. Les fichiers commençant par un point (fichier/dossier caché) ne sont pas listé par `ls` mais le sont par `la`.
  3. Le programme `ls`se situe dans `/usr/bin/ls/`.
  4. Il n'existe pas d'entrée dans le manuel pour `ll`. On apprend avec `alias` que `ll` est l'alias de `ls -alF`.
  5. La commande permettant d'afficher les fichiers contenus dans le dossier `/bin` est `ls /bin`.
  6. La commande `ls` liste le contenu du répertoire.
  7. La commande donnant le chemin complet du dossier courant est `pwd`.
  8. La commande `echo 'bip' > plop` exécutée deux fois crée le fichier `plop` et écrit `bip` dedans puis overwrite ce dernier sur la seconde exécution.
  9. La commande `echo 'bip' >> plop` exécutée deux fois ajoute des `bip` dans le fichier plop.
  10. La commande `sleep 10 | echo 'toto'` attend 10 milliseconds avant d'echo `toto`.
  11. La commande `file` détermine le type d'un fichier.
  12. Lors de l'execution de `lien-phy` on observe qu'il montre le contenu modifié de `original`. Lorsque l'on supprime `original`, `lien_phy` possède toujours le même contenu.
  13. Après la création du lien symbolique, toute modification d'un des deux fichiers exerce la même modification sur l'autre. Après la suppression de `lien_phy`, le fichier `lien_sym` ne peut plus être exécuté/lu. *"No such file or directory"*.
  14. Les raccourcis permettant d'interrompre et de reprendre le défilement sont respectivement `ctrl + s` et `ctrl+q`.
  15. On éxecute dans l'ordre `head -5 /var/log/syslog`, puis `tail -15 /var/log/syslog` et enfin `sed -n '10,20p' /var/log/syslog`.
  16. La commande `dmesg | less` affiche la mémoire tampon du noyau en permettant de revenir en arrière et de la consulter sans possibilité d'écriture.
  17. Ce fichier contient l'ensemble des utilisateurs et les mots de passes cryptés leur étant associé ainsi que les droits de ces utilisateurs. La commande de ce fichier est `man passwd`.
  18. La commande pour afficher par ordre alphabétique inverse la 1ère colonne est `ls -1 | sort -r`.
  19. La commande permettant d'afficher tous les users est `awk -F: '{print $1}' /etc/passwd cut -d: -f1 /etc/passwd`.
  20. La commande permettant de trouver les pages contenant `conversion` est `man --regex -wK 'conversion'`.
  21. La commande utiliser pour trouver tous les fichiers nommés `passwd` est `find . -type f -name "passwd"`.
  22. Pour que le résultat soit dirigé dans `list_passwd_files.txt` on peut faire `find . -type f -name "passwd" > ~/list_passwd_files.txt 2>/dev/null`.
  23. 
