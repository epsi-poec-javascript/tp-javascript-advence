Travaux Pratiques Javascript
# Créer une application en JavaScript Vanilla : TodoList

## Consignes :

Au travers de ce TP, vous allez réaliser une application complète en JavaScript dans le but de découvrir et approfondir des notions clés du langage.

Le TP se veut très progressif, ainsi, vous allez acquérir une certaine autonomie au fur et à mesure de son avancement. Restez consciencieux, notamment en respectant les différentes remarques du cours, car le code source de votre application sera rendu à la fin de la séance. Et bien évidemment il sera noté.

Pour faciliter le rendu et la correction, il vous est demandé d’utiliser l’utilitaire Git ainsi que la plateforme Github. Les quelques commandes vues et pratiquées en cours se suffisent pour ce TP.

La réalisation du projet s’effectue individuellement et sans Internet. Seuls la documentation de Mozilla, les notes de cours et les exercices sont autorisés.
Pour rappel, voici le lien de la documentation : https://developer.mozilla.org/fr/ 

L’idée n’est pas de vous pénaliser, mais plutôt de vous apprendre à utiliser une documentation. Plagier bêtement du code source provenant d’Internet n’aura aucune plus-value sur votre apprentissage de JavaScript. Le TP à pour objectif d’évaluer vos compétences, jouez donc le jeu.

Pour finir, vous allez devoir créer un document qui reprendra toutes les notes de tout ce que vous avez effectué pour réaliser les différentes étapes du TP. Sachez que ce document est à rendre au format PDF dans les sources de votre application. Ces notes pourront vous être très utiles au cours de prochain projet.

## Évaluation :

Le TP sera évalué sur deux points :

- 15 points sont assignés pour la réalisation des différentes tâches du TP
- 5 points sont destinés pour évaluer votre document PDF

Vous pouvez facilement obtenir la moyenne si vous vous appliquez sur la présentation de votre documentation et si vous suivez correctement les consignes de l’exercice. 

*Petit conseil : pour votre documentation, n'hésitez pas à ajouter des captures d’écrans, des schémas ou autres explications que vous jugerez utiles.*

Par ailleurs, toute personne qui ne respecterait pas les consignes pourrait se voir retirer des points.


## Mise en place du projet

De la même manière que ce qui a été vu en cours, commencez par rejoindre le répertoire de l'exercice disponible à cette adresse : https://classroom.github.com/a/43C_UHoY 

Si vous n'êtes pas déjà identifié, faites-le en utilisant les identifiants de votre compte Github.

Ensuite, une page devrait s'afficher et vous demander d'attendre quelques instants avant de recharger votre page.

Un lien devrait ensuite s'afficher, cliquez dessus pour être redirigé dans votre répertoire personnel. Un bouton vert portant le libelle « code » vous permettra d'obtenir l'URL du répertoire, copiez-le.

Ouvrez un terminal et placez-vous dans un dossier où vous pourrez cloner le répertoire grâce à l'instruction suivante :

`git clone <votre_url_de_répertoire>`

Vous pouvez maintenant ouvrir le dossier dans votre éditeur de code et commencer le TP sans soucis.  



**ATTENTION : PENSEZ À EFFECTUER DES « COMMIT » ET DES « PUSH » RÉGULIÈREMENT POUR NE PAS PERDRE VOTRE TRAVAIL.**



En cas de soucis ou d’incompréhension, n'hésitez pas à demander de l'aide à votre intervenant.

BONNE CHANCE À VOUS ! 🙂

## Sommaire

* [**Installation des outils de développement**](docs/setup.md)
  * [Initialiser la gestion de dépendances dans le projet](docs/setup.md#initialiser-la-gestion-de-dépendances-dans-le-projet)
  * [Installer le module bundler Webpack](docs/setup.md#installer-le-module-bundler-webpack)
  * [Lancer l'application dans le navigateur](docs/setup.md#lancer-l-application-dans-le-navigateur)
  * [Vérification de l'outillage et des liens](docs/setup.md#vérification-de-l-outillage-et-des-liens)
  * [Ce que vous avez appris ](docs/setup.md#ce-que-vous-avez-appris--)
* [**Afficher une liste dynamique**](docs/display-list.md)
  * [But de l'exercice](docs/display-list.md#but-de-l-exercice)
  * [Modéliser une liste de tâches dans le JS](docs/display-list.md#modéliser-une-liste-de-tâches-dans-le-js)
  * [Mettre en place un conteneur dans le HTML](docs/display-list.md#mettre-en-place-un-conteneur-dans-le-html)
  * [Afficher les items du tableau dans le HTML](docs/display-list.md#afficher-les-items-du-tableau-dans-le-html)
  * [Vérifier la bonne marche de notre application](docs/display-list.md#vérifier-la-bonne-marche-de-notre-application)
  * [L'avantage du watch avec Wepback](docs/display-list.md#l-avantage-du-watch-avec-wepback)
  * [Ce que vous avez appris](docs/display-list.md#ce-que-vous-avez-appris--)
* [**Ajout d'une nouvelle tâche**](docs/add-item.md)
    * [But de l'exercice](docs/add-item.md#but-de-l-exercice)
    * [Afficher un formulaire dans l'interface (HTML)](docs/add-item.md#afficher-un-formulaire-dans-l-interface--html-)
    * [Ecouter un événement du HTML dans le Javascript](docs/add-item.md#ecouter-un-événement-du-html-dans-le-javascript)
    * [Ce que vous avez appris](docs/add-item.md#ce-que-vous-avez-appris--)
* [**Appels HTTP et API REST**](docs/http.md)
    * [But de l'exercice :](docs/http.md#but-de-l-exercice--)
    * [Créer un projet sur Supabase :](docs/http.md#créer-un-projet-sur-supabase--)
    * [Comprendre comment fonctionne l'API de Supabase](docs/http.md#comprendre-comment-fonctionne-l-api-de-supabase)
    * [Afficher les tâches (Requêtes HTTP et Promesses)](docs/http.md#afficher-les-tâches--requêtes-http-et-promesses-)
        + [Système de Promesses](docs/http.md#système-de-promesses)
        + [Enchaînement de comportements](docs/http.md#enchaînement-de-comportements)
        + [La fonction fetch() de Javascript](docs/http.md#la-fonction-fetch---de-javascript)
    * [Ajouter une tâche dans la base de données](docs/http.md#ajouter-une-tâche-dans-la-base-de-données)
    * [Passer les éléments à "fait" ou "pas fait"](docs/http.md#passer-les-éléments-à--fait--ou--pas-fait-)
    * [Ce que vous avez appris](docs/http.md#ce-que-vous-avez-appris--)
* [**Routing et affichage dynamique**](docs/routing.md)
    * [But de l'exercice :](docs/routing.md#but-de-l-exercice--)
    * [Mise en place et premiers tests](docs/routing.md#mise-en-place-et-premiers-tests)
        + [Premier test : la page d'accueil](docs/routing.md#premier-test---la-page-d-accueil)
        + [Deuxième test : la future page de détails d'une tâche](docs/routing.md#deuxième-test---la-future-page-de-détails-d-une-tâche)
    * [Refactoring pour aller plus loin](docs/routing.md#refactoring-pour-aller-plus-loin)
    * [Gestion dynamique des URLs](docs/routing.md#gestion-dynamique-des-urls)
    * [Page de détails d'une tâche](docs/routing.md#page-de-détails-d-une-tâche)
    * [Ce que vous avez appris](docs/routing.md#ce-que-vous-avez-appris--)
