# TP1
## Exercice 2
### Manuel
**1. A l’aide du manuel, identifiez le rôle de la commande which**

```$ man which```  
which : renvoie le chemin d'accés du fichier de la commande concernée

**2. Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercherle terme option dans la page de manuel de which?**

Dans le man taper: ```/motRecherché``` 
    
**3. Comment quitte-t-on le manuel?**

``q``

**4. Chaque section du manuel a une première page, qui présente le contenu de la section. Aﬀicher la première page de la section 6; de quoi parle cette section?**

```man 6 intro``` 
La page parle des jeux et des fonctionnalités amusantes disponible sur l'OS.

### Navigation dans l’arborescence des fichiers
**1. allez dans le dossier /var/log**

 ```cd /var/log/```
 
**2. remontez dans le dossier parent (/var) en utilisant un chemin relatif**

```cd ..```

**3. retournez dans le dossier personnel**

```cd ~```

**4. revenez au dossier précédent (/var)sans utiliser de chemin**

```cd -```

**5. essayez d’accéder au dossier /root; que se passe-t-il?**

```cd /``` 
On ne peut pas y accèder car nous n'avons pas les droits sur le dossier (dossier du super utilisateur).

**6. essayez la commande sudo cd /root; que se passe-t-il? Explique**

Cela ne fonctionne pas car ```cd``` est une commande interne a l'OS est n'est pas présente dans les dossiers de la variable PATH de l'utilisateur.

**7. à partir de votre dossier personnel, créez l’arborescence suivante**  

```
$ mkdir -p {Dossier1,Dossier2/{Dossier2.1,Dossier2.2}}
$ touch Dossier2/Dossier2.2/{fichier2,fichier3}
$ touch Dossier1/fichier1
```

**8. revenez dans votre dossier personnel; à l’aide de la commande rm, essayez de supprimer Fichier1, puisDossier1; que se passe-t-il?**

On ne peut pas supprimer un dossier avec la commande rm sans utiliser une option de forçage.

**9. quelle commande permet de supprimer un dossier?**

``` rmdir ```

**10. que se passe-t-il quand on applique cette commande à Dossier2?**

On a une erreur expliquant que le dossier n'est pas vide.

**11. comment supprimer en une seule commande Dossier2 et son contenu?**

``` rm -r Dossier2 ```

### Commandes importantes

**1. Quelle commande permet d’aﬀicher l’heure? A quoi sert la commande time?**

La commande ```date``` permet d'afficher l'heure.

La commande ```time``` sert à retourner le temps d'execution d'une commande. 

**2. Dans votre dossier personnel, tapez successivement les commandes ls puis la; que peut-on en déduire sur les fichiers commençant par un point?**

```la``` affiche en plus les fichier et dossier caché.

**3. Où se situe le programme ls?**

/usr/bin/ls

**4. Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.**
 
 Non il n'y a pas de page de manuel car c'est un racourcis de la commande ```ls -l```

**5. Quelle commande permet d’aﬀicher les fichiers contenus dans le dossier/bin?**

```ls /bin```

**6. Que fait la commande ls ..?**

Elle liste les fichier et dossier présent dans le repertoire parent du repertoire courant.

**7. Quelle commande donne le chemin complet du dossier courant?**

```pwd```

**8. Que fait la commande echo 'yo' > plop exécutée 2 fois?**

Elle remplace le contenu du fichier plop (en le créant si inexistant).

**9. Que fait la commande echo 'yo' >> plop exécutée 2 fois?**

Elle concatène à la suite dans le fichier plop

**10. A quoi sert la commande file? Essayez la sur des fichiers de types différents.**

Elle retourne le type du fichier renseigné.

**11. Créez un fichier toto qui contient la chaîne Hello Toto !; créer ensuite un lien titi vers ce fichier avec la commande ln toto titi. Modifiez à présent le contenu de toto et aﬀichez le contenu de titi: qu’observe-t-on? Supprimez le fichier toto; quelle conséquence cela a-t-il sur titi?**

La modification de l'un entraine la modification de l'autre mais la suppression de l'un n'entraine pas la suppresion de l'autre.

**12. Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez lecontenu de titi; quelle conséquence pour tutu? Et inversement? Supprimez le fichiertiti; quelleconséquence cela a-t-il surtutu?**

La modification ou suppresion de l'un entraine la modification ou suppression de l'autre.

**13. Aﬀichez à l’écran le fichier/var/log/syslog. Quels raccourcis clavier permettent d’interrompre etreprendre le défilement à l’écran?**

CTRL + S

**14. Aﬀichez les 5 premières lignes du fichier/var/log/syslog, puis les 15 dernières, puis seulement les lignes 10 à 20.**

Pour afficher les 5 premières lignes: ```head -5 /var/log/syslog```

Pour afficher les 15 dernières lignes: ```tail -15 /var/log/syslog```

Pour afficher les lignes 10 à 20: ```sed -n '10,20p' /var/log/syslog```

**15. Que fait la commande dmesg | less?**

La commande ```dmesg``` affiche le buffer du noyau. L'option ```less``` permet d'afficher le contenu page par page et permet de naviguer.

**16. Aﬀichez à l’écran le fichier /etc/passwd; que contient-il? Quelle commande permet d’aﬀicher la page de manuel de ce fichier?**

Le fichier /etc/passwd contient les mots de passe chiffrés des utilisateurs.

La commande ```man passwd``` permet d'afficher la page de manuel de ce fichier.

**17. Aﬀichez seulement la première colonne triée par ordre alphabétique inverse**

Pour afficher la première colonne du fichier /etc/passwd triée par ordre alphabétique inverse, il faut taper respectivement les 2 commandes suivantes :

```cut -c1 /etc/passwd > test.txt```

```sort -r test.txt```

**18. Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seule-ment les utilisateurs connectés)?**

```wc -l /etc/test.txt``` (permet de compter le nombre de lignes du fichier créé dans la question précédante et donc le nombre d'utilisateurs.)

**19. Combien de pages de manuel comportent le mot-clé conversion dans leur description?**

```man -k conversion | wc -1```

**20. A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine**


```find -name passwd```

**21. Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier~/list_passwd_files.txtet que les erreurs soient redirigées vers le fichier spécial/dev/null**

```find -name passwd > list_passwd_files.text 2 > /dev/null```

**22. Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu précédemment**

L'alias ll est défini dans le fichier .bashrc.

**23. Utilisez la commande locate pour trouver le fichier history.log.**

Avec la commande ```locate history.log``` on voit que ce fichier est situé dans /var/log/apt/history.log

**24. Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il? Pourquoi?**

On ne trouve pas le fichier créé dans le dossier personnel avec la commande "locate" puisque le fichier n'a pas été ajouté à la base de données que parcourt la commande locate. Il faut rafraîchir cette base de données pour afficher le dossier avec la commande ```updatedb```.

## Exercice 4

**3. Le fichier .bashrc est lu au démarrage du shell; pour le recharger, il faudrait donc se déconnecter puis se reconnecter; mais il existe un autre moyen : la commande source .bashrc. Testez-la, l’invite de commande devrait immédiatement passer en couleurs.**

La commande ```source .bashrc``` permet de recharger le fichier .bashrc.

**4. Les couleurs par défauts (surtout celle du dossier courant) ne sont pas très visibles. Dans .bashrc, cherchez les lignes commençant par PS1=; elles indiquent la mise en forme de l’invite de commande (selon que l’on est en couleurs ou non).**

```\e[35m[\A] - ${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;36m\]\w\[\033[00m\]\$```
