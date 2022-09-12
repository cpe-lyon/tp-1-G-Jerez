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
  7. 
