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

