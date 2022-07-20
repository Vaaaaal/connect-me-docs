---
sidebar_position: 2
---

# Pour commencer

## Installation

Pour commencer à développer sur Connect-Me vous aurez besoin d'installer :
- [Cordova](https://cordova.apache.org/)
- [cordova-res](https://cordova.apache.org/https://www.npmjs.com/package/cordova-res)
- [Node.js](https://nodejs.org/en/download/)

## Configuration

Vous devrez également ajouter les plateformes sur lesquels vous souhaitez déployer votre projet afin de générer le code via Cordova.

Nous aurons besoin d'ajouter IOS, Android et browser.
Pour cela, rendez vous dans le dossier `./src-cordova` et utiliser les commandes suivante :
```bash
cordova add ios
cordova add android
cordova add browser
```

Puis, après vérification via la cmd `cordova requirements`, installer [tous les services](https://cordova.apache.org/docs/en/11.x/guide/cli/index.html#install-pre-requisites-for-building) manquant dont vous pourriez avoir besoin pour utiliser les plateformes que vous venez d'ajouter.

Enfin, générer les icônes avec la commande `cordova-res` après avoir installer la librairie afin de pouvoir lancer le projet.

## Problèmes possible

En lançant l'application avec IOS vous allez peu-être rencontrer une erreur de ce type :
```
Error: doc.find is not a function
```
Vous pouvez régler le problème en exécutant cette commande [(lien vers les explications)](https://stackoverflow.com/a/66644339)
```bash
cordova platform rm ios && cordova platform add ios
```

:::warning Mac M1
Si vous utilisez un MacBook équipé d'une puce M1, vous allez rencontrer des problèmes pour faire tourner le simulateur IOS via xCode, pour tester votre application vous devrez donc connecter un iPhone via USB.
:::