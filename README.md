# Mon Projet

## Description
Ce projet est une API simple construite avec Node.js et Express.js qui se connecte à une base de données MySQL. Il inclut des points de terminaison pour récupérer et mettre à jour des données.

## Fonctionnalités
- Connexion à une base de données MySQL
- Récupération des données avec des requêtes GET
- Mise à jour des données avec des requêtes PUT

## Installation

1. Clonez le dépôt :
    ```sh
    git clone https://github.com/votre-utilisateur/votre-repo.git](https://github.com/nabilabel123/Projet.git)
    ```
2. Accédez au répertoire du projet :
    ```sh
    cd Projet
    ```
3. Installez les dépendances :
    ```sh
    npm install
    ```

## Configuration

   1. Mettez à jour la configuration de la base de données dans `db.js` :
    ```javascript
    const mysql = require('mysql2');

    const db = mysql.createConnection({
      host: 'localhost',
      user: 'root',
      password: '',
      database: 'my_projet'
    });

    db.connect((err) => {
      if (err) {
        console.error('Erreur de connexion à la base de données:', err);
      } else {
        console.log('Connecté à la base de données');
      }
    });

    module.exports = db;
    ```

## Utilisation

1. Démarrez le serveur :
    ```sh
    node api.js
    ```

2. Utilisez Postman ou tout autre client API pour tester les points de terminaison.

### GET /data
Récupérer toutes les données de la base de données.
- URL : `http://localhost:3000/data`
- Méthode : `GET`

### PUT /data/:id
Mettre à jour les données dans la base de données.
- URL : `http://localhost:3000/data/:id`
- Méthode : `PUT`
- Corps :
    ```json
    {
  "sender_id": 1,
  "recipient_id": 2,
  "content": "N’oublie pas de soumettre ton devoir avant demain.",
  "course_id": 1,
  "status": " lu"
}
    ```

