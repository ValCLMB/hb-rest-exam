# PHP Webservices REST - Examens

Pour travailler sur ce projet :

- **créer un fork** du projet (sur la page [git@github.com:Dreeckan/hb-rest-exam.git](git@github.com:Dreeckan/hb-rest-exam.git), cliquer sur le bouton `fork`, en haut à droite de la page)
- Cloner **votre** projet (commande `git clone` par exemple)
- Créer une branche pour faire tout l'exam
- Toutes les modifications vont se faire dans ce même fichier.
- À la fin de l'examen, vous **devez** envoyer un zip de votre code _via_ Discord et vous **pouvez** faire une PR à destination du projet d'origine (afin de faciliter mes retours pour la correction)

La durée prévue est d'environ 2h. Des points peuvent être perdus pour le retard du rendu :

- 1 point si le rendu est fait après 18h
- 2 points si le rendu est fait après 20h

## Liste des questions et barème

1. Une API, qu'est-ce que c'est ? (1 point)
2. Peut-on récupérer ces informations avec une API ? (1 point)
3. XML et JSON (2 points)
4. Définitions (5 points)
5. Les grands principes de REST (5 points)
6. Les status HTTP (3 points)
7. Comment se connecter à une API ? (2 points)
8. Comment (dans l'idéal) connait-on les endpoints et les retours d'une API ? (1 point)

## Questions à choix multiples

Pour chacune des questions présentes dans ce test, il vous est précisé si plusieurs réponses sont possibles. Vous ne perdez pas de points pour une mauvaise réponse, mais toutes les bonnes réponses doivent être cochées pour obtenir tous les points. Une mauvaise réponse cochée annule une bonne réponse cochée.

### 1. Qu'est-ce qu'une API ? (une seule réponse)

- [x] Un intermédiaire pour communiquer entre une application et une base de données
- [ ] Un protocole pour remplacer HTTP
- [ ] Une manière de coder en Symfony, expliquant comment ranger les fichiers et différentes normes à utiliser

### 2. Peut-on faire ceci avec une API ? (plusieurs réponses)

- [x] Récupérer un tweet de Chris Pratt (acteur américain)
- [ ] Pirater la NASA
- [x] Obtenir les vols disponibles pour un trajet Lyon - Paris
- [x] Se connecter grâce à Facebook sur un site autre
- [ ] Obtenir le mot de passe Facebook d'Emmanuel Macron

### 3. XML et JSON

#### 3.1. Qu'est-ce que XML ? (une seule réponse)

- [ ] Un langage de programmation orienté objet
- [x] Un méta-langage de balisage
- [ ] Un groupe de rock qui a fait fureur dans les années 70

#### 3.1. Qu'est-ce que JSON ? (une seule réponse)

- [ ] Un célèbre auteur de romans policiers
- [ ] Un langage de programmation orienté objet
- [x] Un format de données textuelles
- [ ] Une extension de javascript, seul moyen d'utiliser AJAX

### 4. Définitions

#### 4.1. Qu'est-ce que REST ? (une seule réponse)

- [ ] Un protocole (comme HTTP) de communication entre une ou des applications mobiles et un serveur tiers
- [ ] Une méthode du protocole HTTP, comme GET, POST ou PATCH, permettant les échanges entre une API et une application
- [x] Un style d'architecture logicielle, définissant des contraintes d'interopérabilité entre différents logiciels

#### 4.2. Quel protocole utilise une API REST (ou RESTful) ? (une seule réponse)

- [ ] REST
- [x] HTTP
- [ ] PHP
- [ ] JSON

#### 4.3. Parmi ceux présentés, quels sont les verbes (ou méthodes) disponibles dans une API REST ? (plusieurs réponses)

- [ ] REST
- [ ] JSON
- [x] GET
- [x] POST
- [ ] PHP

#### 4.4. Nommage

Nous allons utiliser des exemples de [cette API sur Game Of Thrones](https://anapioficeandfire.com/Documentation) pour le nom des éléments, en REST.
Pour toutes ces questions, seule une réponse est vraie.

##### 4.4.1. Qu'est-ce que `https://www.anapioficeandfire.com/api/books` ?

- [x] Une URL
- [ ] Un endpoint / une URI
- [ ] Une collection
- [ ] Une ressource

##### 4.4.2. Dans ce même exemple, qu'est-ce que `/books` ?

- [ ] Une URL
- [x] Un endpoint / une URI
- [ ] Une collection
- [ ] Une ressource

##### 4.4.3. Dans ce même exemple, comment appelle-t-on le retour ?

```json
[
  {
    "url": "https://www.anapioficeandfire.com/api/books/1",
    "name": "A Game of Thrones",
    "characters": [
      "https://www.anapioficeandfire.com/api/characters/2",
      ...
    ],
    "povCharacters": [
      "https://www.anapioficeandfire.com/api/characters/148",
      ...
    ]
  },
  ...
 ]
```

- [ ] Une URL
- [ ] Un endpoint / une URI
- [x] Une collection
- [ ] Une ressource

##### 4.4.4. Enfin, comment appelle-t-on ce retour ?

```json
{
  "url": "https://www.anapioficeandfire.com/api/books/1",
  "name": "A Game of Thrones",
  "isbn": "978-0553103540",
  "authors": [
    "George R. R. Martin"
  ],
  "numberOfPages": 694,
  "publisher": "Bantam Books",
  "country": "United States",
  "mediaType": "Hardcover",
  "released": "1996-08-01T00:00:00",
  "characters": [
    "https://www.anapioficeandfire.com/api/characters/2",
    ...
  ],
  "povCharacters": [
    "https://www.anapioficeandfire.com/api/characters/148",
    ...
  ]
}
```

- [ ] Une URL
- [ ] Un endpoint / une URI
- [ ] Une collection
- [x] Une ressource

### 5. Les grands principes de REST

#### 5.1. Dans une relation client-serveur, qu'est-ce que le client ? (plusieurs réponses possibles)

- [x] Une application qui demande des données au serveur
- [ ] Un programme qui répond aux requêtes
- [ ] Une base de données
- [x] Un programme qui va afficher des informations à l'utilisateur
- [ ] Un composant indépendant utilisant les données renvoyées par le serveur

#### 5.2. Dans un système sans état, le serveur se souvient-il des requêtes des clients ? (une seule réponse)

- [ ] Oui
- [x] Non

#### 5.3. Dans un système en couche, le client sait-il directement le contenu de la base de données et son organisation ? (une seule réponse)

- [ ] Oui
- [x] Non

#### 5.4. Dans un système en couche, le client sait-il s'il communique avec une ou plusieurs API ? (une seule réponse)

- [ ] Oui
- [x] Non

#### 5.4. À quoi sert la mise en cache des réponses ? (plusieurs réponses possibles)

- [x] À diminuer le temps de calcul
- [ ] À ne pas montrer certaines informations au client
- [x] À ne pas renvoyer plusieurs fois la même information

#### 5.5. Que permet une interface uniforme ? (plusieurs réponses possibles)

- [x] Client comme serveur savent comment communiquer ensemble
- [x] Appliquer une modification côté serveur applique automatiquement la même modification sur les clients
- [ ] Un client écrit en java peut récupérer des informations d'un site codé en PHP

### 6. Les status HTTP

#### 6.1. Que représentent les statuts HTTP entre 200 et 299 ? (une seule réponse)

- [ ] Des erreurs côté serveur
- [x] Une opération réalisée avec succès
- [ ] Un statut interne à HTTP
- [ ] Une redirection
- [ ] Des erreurs côté client

#### 6.2. Que représentent les statuts HTTP entre 500 et 599 ? (une seule réponse)

- [x] Des erreurs côté serveur
- [ ] Une opération réalisée avec succès
- [ ] Un statut interne à HTTP
- [ ] Une redirection
- [ ] Des erreurs côté client

#### 6.3. Que représentent les statuts HTTP entre 400 et 499 ? (une seule réponse)

- [ ] Des erreurs côté serveur
- [ ] Une opération réalisée avec succès
- [ ] Un statut interne à HTTP
- [ ] Une redirection
- [x] Des erreurs côté client

### 7. Comment se connecter à une API ? (plusieurs réponses possibles)

- [ ] Avec un formulaire de connexion sur le serveur
- [x] Avec un token API (une chaine de caractères spécifique à un utilisateur)
- [x] Avec un identifiant et un mot de passe
- [ ] Par email

### 8. Comment (dans l'idéal) connait-on les endpoints et les retours d'une API ? (plusieurs réponses possibles)

- [ ] En testant des urls au hasard
- [x] En lisant la documentation de l'API
- [ ] En découvrant différents endpoints dans les retours des requêtes
- [x] En utilisant Postman ou un outil du navigateur qui va nous donner toutes les routes possibles
