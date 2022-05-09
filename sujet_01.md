# Examen

Dans une application sécurisée par vos soin avec Node/Express, et d'autres technologies, vous allez développer une interface permettant de faire des statistiques sur un Dataset spécifique : le titanic.

L'utilisation de React pour l'interface utilisateur peut être utilisé. Vous pouvez utiliser Symfony pour développer une API, avec React éventuellement.

L'objectif de l'application et d'afficher les survivants du Titanic en fonction du sex, de l'age et de la classe des billets.

Vous apporterez un soin particulier au rendu des statistiques.

La piste graphique à suivre est le design Web de l'application kaggle.com.

## Contraintes techniques

- Vous devez faire un trello pour organiser/planifier les étapes de conception.

- Votre code sera versionné à l'aide de Git sur Github ou Gitlab.

- Utilisez Node.js, Express et un moteur de rendu comme pug ou twing. React peut-être également utiliser pour la partie "front".

- Si vous n'avez pas vu Node.js vous pouvez utiliser Symfony pour la partie API et React ou Angular.

- Vous devez également créer une persistance pour les données avec MySQL ou MongoDB avec Mongoose pour Node.js et l'intégrer à l'API ou à l'application.

- Il faudra également mettre en place une page de login pour consulter/lancer la création des statistiques.

- Vous devez faire la partie interface utilisateur à partir du chapitre qui suit ci-dessous.

## Analyse des données & pages à réalisées

*Vous pouvez utiliser MongoDB, pour analyser les données. Suivez dans ce cas les étapes ci-dessous.*

1. Importez les données au format CSV à l'adresse suivante : https://raw.githubusercontent.com/hkacmaz/Titanic-Passenger-Survivors/master/train.csv

Puis tapez la ligne de commande suivante, notez l'option **headerline** qui indique les clés des valeurs du Dataset.

```bash
mongoimport --db titanic --collection passengers --type=csv --headerline --file train.csv --drop
```

2. Créez la page de login, page principale de l'application. Une fois connecté on sera redirigé vers la page pour lancer les analyses statistiques.

3. Créez la page de recherche à proprement parlée, elle comportera un menu principale permettant de se connecter et déconnecter.

```text
Sex : [] Age : [] Classe []
[Analyser]
```

Une fois la recherche effectuée vous redirigerez l'utilisateur vers une page proposant un graphique de votre choix pour expliciter chacun des résultats. Un bouton Reset permettra d'effacer la recherche et de revenir à la page précédente.

```text

Graphique

[Reset]

```

4. Améliorez maintenant l'analyse des données

Introduisez les éléments suivants dans la rechercher

- La moyenne

- L'écart type

5. Proposez une autre recherche sur l'analyse de ses données.