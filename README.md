# Last Deals

Last Deals est une application fonctionnant sur electron qui permet d'afficher les derniers deals existant sur https://www.dealabs.com/

### Pre-requis 

Il est nécessaire pour faire fonctionner l'application d'installer Electron

#### Installer Electron

Il faut utiliser NPM pour installer et démarrer Electron.

```
npm install electron --save-dev --save-exact
```

Pour éxecuter electron il suffit de se positionner dans le répertoire electron quick start et d'éxécuter la commande suivante :
```
npm start
```

## Comment utiliser l'application

Il n'y a rien à faire, l'application liste automatiquement les derniers deals.

## Mode opératoire sur la création de l'application

**Etape 1 :**

J'ai tout d'abord essayer de repérer s'il existait un flux RSS sur le site ou un autre flux de données disponible qui m'éviterait de devoir parser en brut la page du site dealabs.

J'ai trouvé le flux RSS au format XML : https://www.dealabs.com/rss/tout


**Etape 2 :**

Je récupère les données XML avec une requête Ajax en jQuery avec $.get() et je boucle sur l'objet pour récupérer les éléments qui m'interesse avec un .find() sur les namespaces de mon XML.


**Etape 3 :**

Ensuite, on essaie de profiter de la boucle .each() pour implémenter dans le corps de notre fichier html les "deals" en pointant leur concaténation sur un sélecteur précis ".deal".


**Etape 4 :**

On stylise notre page avec une feuille de style CSS et le grid system de bootstrap.

-----------------
## Auteur

* **Yacine Souadda** - [Luwata](https://github.com/luwata)