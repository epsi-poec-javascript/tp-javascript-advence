# Installation de dépendances de développement

Le Web et les navigateurs ont beaucoup évolué depuis leur création, notamment en proposant des fonctionnalités très intéressantes pour nos applications. Malgré une amélioration de la performance des connexions Internet, l’optimisation des performances pour les applications devient le nerf de la guerre.

C’est d’ailleurs sur l’une de ces caractéristiques que s’appuie le bot de Google visant à référencer les différents sites dans son moteur de recherche. Google force toutes les applications du Web à accroitre leurs performances pour se placer dans les premiers résultats de recherche, on parle notamment de SEO.

Auparavant cela n’aurait jamais pu être possible. Mais avec l’évolution des technologies, il est maintenant possible de se constituer un environnement qui va se composer de tous les outils nécessaires au développement dit moderne.

## Sommaire :

- [Installation de dépendances de développement](#installation-de-dépendances-de-développement)
  - [Sommaire :](#sommaire-)
  - [Premier constat](#premier-constat)
  - [Initialiser la gestion de dépendances dans le projet](#initialiser-la-gestion-de-dépendances-dans-le-projet)
  - [Installer le module bundler Webpack](#installer-le-module-bundler-webpack)
  - [Vérification de l'outillage et des liens](#vérification-de-loutillage-et-des-liens)
- [Ce que vous avez appris :](#ce-que-vous-avez-appris-)

## Premier constat

Commencez par créer un fichier « index.html » en complétant la structure de base et créez un fichier `script.js` dans le dossier `assets/js/`.

Admettons que le fichier JavaScript « script » sera celui qui contiendra votre code principal pour l’application. Dans ce fichier, écrivez l’instruction pour afficher le texte « Mon fichier principal » dans la console.

En regardant la console, nous devrions simplement obtenir le message que nous avons demandé d’afficher et certainement une erreur au sujet d’un favicon non trouvé. Ceci est tout à fait normal.

Dirigez-vous maintenant dans l’onglet « Réseau » de votre console.

1. Que remarquez-vous ?
2. Expliquez la problématique perçue au travers de votre remarque.

Pour rendre l’application beaucoup plus attrayante, vous allez installer la bibliothèque « FontAwesome ». Celle-ci ajoute une multitude d’icônes pouvant être utilisées au sein des pages de l’application. Vous retrouverez la bibliothèque à cette adresse : [https://fontawesome.com/](https://fontawesome.com/https:/).

Pour cela vous utiliserez ces deux liens :

* Le fichier CSS disponible à cette adresse : `https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.0/css/all.min.css`
* Le fichier JS disponible à cette adresse : `https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.0/js/all.min.js`

Ces deux liens font référence à un CDN (Content Delivery Network), ils délibèrent des ressources en choisissant le serveur le plus proche de la position géographique de l’Internaute.

Une fois que vous avez intégré ces deux liens dans votre page HTML, vous pouvez vérifier que la bibliothèque fonctionne correctement en ajoutant cette balise à la fin du texte de votre titre :

`<i class="fa-solid fa-cloud"></i>`

Vous devriez voir apparaitre un nuage. Il est également possible de personnaliser l’icône que vous souhaitez afficher. Vous pouvez accéder à la page listant toutes les icônes ici : [https://fontawesome.com/search](https://fontawesome.com/searchhttps:/)

Attention : certaines icônes sont payantes, pensez à bien filtrer les icônes gratuites dans les paramètres de recherche.

Cette intégration de bibliothèque n’est pour le moment pas problématique même si elle n’arrange en rien le premier constat que vous avez fait. Imaginez si le nombre de bibliothèques venait à se multiplier, leur gestion deviendrait beaucoup trop compliquée.

Au travers de ces deux constats, vous devez comprendre qu’il devient aujourd’hui nécessaire d’organiser son environnement de développement afin d’adopter les bons outils et ainsi assurer la qualité de son application.

L’élément clé c’est le gestionnaire de dépendance.

## Initialiser la gestion de dépendances dans le projet

Depuis la modernisation du JavaScript, notamment en rendant possible son exécution côté serveur à NodeJS, le nombre d’outils et de bibliothèques a très largement augmenté.

Comme tout bon langage serveur qui se respecte, NodeJS intègre lui aussi un gestionnaire de dépendances. Même s’il existe d’autres alternatives, c’est principalement Node Package Manager (NPM) qui va jouer ce rôle de chef d’orchestre.

Il faut savoir qu’un gestionnaire de dépendance, aussi appelé package manager, va-vous aider à installer, lister, supprimer et mettre à jour toutes les dépendances (librairies) dont votre projet aura besoin pour fonctionner.

Pour pouvoir bénéficier de la puissance de NPM, il va vous falloir installer NodeJS. Selon votre système d’exploitation, voici les manipulations à effectuer :

**Windows :**
Sur Windows, rendez-vous sur [https://nodejs.org/fr/](https://nodejs.org/fr/https:/) et téléchargez la version LTS (long terme support). Exécutez le fichier que vous venez de télécharger et suivez les étapes d’installations. Vous n’avez pas besoin de modifier quoique ce soit, laissez les paramètres par défauts.

**macOS :**
Pour macOS, il vous suffit d’ouvrir un terminal et de lancer la commande « brew install node »

Pour tester que tout fonctionne correctement essayez d’exécuter `node -v` et `npm -v` chacune de ces commandes devrait vous retourner un numéro de version.

Dans le cas où cela ne fonctionne pas :

* Si vous avez utilisé la console de votre éditeur de code, veuillez le fermer et le rouvrir avant de tester à nouveau.
* Sinon vérifiez la variable d’environnement de votre système d’exploitation.

Dans votre projet, vous pouvez désormais créer le manifeste permettant la configuration de celui-ci.

Vous pouvez faire cela très facilement grâce à la commande `npm init -y`.

Cette commande doit vous faire apparaitre votre manifeste qui se nomme  `package.json`. Ce fichier contient en fait toutes les informations relatives à votre projet. Il va par exemple stocker la liste des librairies installées dans votre projet.

Essayez d’installer FontAwesome depuis NPM en lançant la commande suivante : `npm install --save @fortawesome/fontawesome-free`

1. Que remarquez-vous ? Veillez à bien détailler votre réponse.

Remplacez maintenant les liens de votre page HTML :

* Pour le fichier CSS, utilisez `node_modules/@fortawesome/fontawesome-free/css/all.css`
* Pour le fichier JS, utilisez `node_modules/@fortawesome/fontawesome-free/js/all.js`

Si vous ouvrez votre fichier « package.json », vous devriez normalement voir figurer FontAwesome dans la liste des dépendances.

## Installer le module bundler Webpack

Dans le monde du front, la rapidité d'affichage d'une page est une clé de la réussite. Divers patterns ont été imaginés pour réussir à obtenir une meilleure rapidité dans le chargement d'une page.

L'un d'eux est le "bundling" qui consiste à :

1. Permettre aux developpeuses et développeurs de coder dans différents fichiers afin d'organiser le code au mieux ;
2. Ne livrer malgré tout qu'un seul fichier JS au navigateur lors de la visite de la page (et donc améliorer temps de chargement en réduisant le nombre de requêtes HTTP concernant la récupération du Javascript) ;

L'outil le plus connu (et d'aucuns diraient le plus puissant et configurable) pour arriver à ce résultat est Webpack. Nous allons donc l'installer grâce à la commande suivante :

`npm install --save-dev webpack webpack-cli`

Une fois l'outil installé, il faut absolument le configurer pour lui expliquer où sont les fichiers qui contiennent le code de base, et où doit-il écrire le fichier unique final qui sera ensuite livré au navigateur :

```js
// webpack.config.js

// Permet de résoudre des chemins de fichiers
const path = require("path");

module.exports = {
  // Le fichier qui sert de point d'entrée et qui importe les différentes dépendances de l'application
  entry: "./src/app.js",
  // Le dossier et nom du fichier qui sera généré par Webpack après le build
  // Webpack va donc intégrer l'ensemble des modules (dépendances) nécessaires dans un seul fichier dist/app.js
  output: {
    filename: "app.js",
    path: path.resolve(__dirname, "dist"),
  },
};
```

Il faut ensuite permettre aux développeurs de lancer Webpack lorsqu'ils le souhaitent, pour cela nous allons configurer NPM et ajouter un script. Ce que nous disons ci-dessous, c'est que lorsqu'on demandera à NPM le script **dev**, celui ci lancera la commande `webpack --mode development`

```json
// package.json

"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "webpack --mode development"
},
```

Pour tester cette nouvelle tâche, nous lançons simplement la commande suivante : `npm run dev` et webpack devrait générer le fichier *dist/app.js*

## Vérification de l'outillage et des liens

Maintenant qu'on a mis en place les outils de base, nous allons vérifier que tout fonctionne.

Premièrement, ajoutez le code suivant dans le fichier *src/app.js*

```js
// src/app.js
console.log("Tout fonctionne");
```

Puis modifiez le fichier *index.html* afin d'ajouter à la toute fin du `<body>` la balise suivante, qui permettra de demander au navigateur de télécharger le fichier construit par webpack :

```html
<script src="dist/app.js"></script>
```

Notez que pour l'instant, le fichier dist/app.js ne contient absolument pas le code qu'on a ajouté à src/app.js, pour cela il faudrait appeler Webpack afin qu'il prenne en compte le changement : `npm run dev`

Vous pouvez maintenant aller sur votre navigateur et ouvrir la console de développement afin de vous assurer que vous obtenez bien le message **"Tout fonctionne"**.

# Ce que vous avez appris :

* Utiliser NPM afin de gérer les dépendances (librairies ou outils) nécessaires à votre projet ;
* Utiliser NPM afin de configurer des tâches que vous pourrez lancer ;
* Utiliser Webpack pour "bundler" vos fichiers JS en un fichier unique (et bien plus) ;
* Utiliser live-server afin de créer un petit serveur web et d'afficher votre application dans le navigateur ;

[Revenir au sommaire](../README.md) ou [Passer à la suite : Afficher la liste des tâches](display-list.md)
