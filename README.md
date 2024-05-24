# Application de Gestion de Tâches en React

## Description
Il s'agit d'une application React simple pour gérer une liste de tâches. Elle démontre les concepts de base de React, y compris les composants, l'état et les props.

## Structure du Projet
Le projet a la structure suivante :

```
my-app/
├── public/
│   ├── index.html
├── src/
│   ├── components/
│   │   ├── Header.js
│   │   ├── Footer.js
│   │   └── TodoItem.js
│   ├── App.js
│   ├── index.js
│   ├── config.js
│   └── styles.css
├── Dockerfile
├── package.json
└── README.md
```

## Comment Lancer
### Sans Docker
1. **Installer les dépendances** : `npm install`
2. **Démarrer le serveur de développement** : `npm start`
3. Ouvrez [http://localhost:3000](http://localhost:3000) pour voir l'application dans le navigateur.

### Avec Docker
1. **Construire l'image Docker** : `docker build -t my-app .`
2. **Lancer le conteneur Docker** : `docker run -p 5000:5000 my-app`
3. Ouvrez [http://localhost:5000](http://localhost:5000) pour voir l'application dans le navigateur.

## Composants
- **Header** : Affiche le titre de l'application.
- **Footer** : Affiche les informations du pied de page.
- **TodoItem** : Représente une tâche unique. Permet de basculer l'état de complétion.

## Gestion de l'État
L'état est géré dans le fichier `App.js` en utilisant le hook `useState`. L'état `todos` garde la trace de la liste des tâches et de leur statut de complétion.

## Configuration de MongoDB
Une configuration de base de MongoDB est incluse dans le fichier `src/config.js`. L'application s'attend à une URI MongoDB dans la variable d'environnement `MONGO_URI`. Si elle n'est pas fournie, elle utilise par défaut `mongodb://localhost:27017/myapp`.

## Styles
Les styles de base sont définis dans le fichier `src/styles.css`.