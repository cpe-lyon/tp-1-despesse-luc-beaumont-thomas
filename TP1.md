# TP1
## Exercice 2
### Manuel
**1. A l’aide du manuel, identifiez le rôle de la commande which**

```$ man which```  
which : renvoie  le chemin des fichiers (ou liens) qui seraient exécutés dans l'environnement courant si ses arguments avaient été donnés  comme commandes  dans un interpréteur de commandes strictement conforme à PO‐SIX. Pour ce faire, which cherche dans la variable  PATH  les  fichiers exécutables  correspondant  aux  noms des arguments. which ne normalise pas les chemins.

**2. Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercherle terme option dans la page de manuel de which?**

Dans le man taper ```/motRecherché``` 
    
**3. Comment quitte-t-on le manuel?**

``q``

**4. Chaque section du manuel a une première page, qui présente le contenu de la section. Aﬀicher la première page de la section 6; de quoi parle cette section?**

``man 6 intro`` La page parle des jeux et des fonctionnalités amusante dispo sur l'OS.

### Navigation dans l’arborescence des fichiers
**1. allez dans le dossier /var/log**

 ``cd /var/log/``
 
**2. remontez dans le dossier parent (/var) en utilisant un chemin relatif**

``cd ..``
**3. retournez dans le dossier personnel**

``cd ~``
**4. revenez au dossier précédent (/var)sans utiliser de chemin**
``cd -``
**5. essayez d’accéder au dossier /root; que se passe-t-il?**
``cd /`` On ne peut pas y accèder car nous n'avons pas les droits sur le dossier (dossier du super utilisateur)
**6. essayez la commande sudo cd /root; que se passe-t-il? Explique**

**7. à partir de votre dossier personnel, créez l’arborescence suivante**  
## Exercice 3

