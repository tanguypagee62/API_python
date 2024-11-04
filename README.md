# Documentation de l'API

Cette API permet de gérer une collection de livres, incluant les fonctionnalités CRUD dans une base de données SQLite.

## Endpoints

### 1. Récupérer tous les livres
- **URL** : `/books`
- **Méthode** : `GET`
- **Description** : Retourne une liste de tous les livres disponibles.
- **Commande `curl`** : curl -X GET http://127.0.0.1:5000/books

### 2. Récuperer un livre par ID
- **URL** : `/books/<book_id>`
- **Méthode** : `GET`
- **Paramètres** : `book_id` : ID du livre à récupérer.
- **Description** : Retourne les détails d'un livre spécifique.
- **Commande `curl`** : curl -X GET http://127.0.0.1:5000/books/1

### 3. Ajouter un nouveau livre
- **URL** : `/books`
- **Méthode** : `POST`
- **Headers** : `Content-Type: application/json`
- **Body** : `{"title": "Titre du livre", "author": "Nom de l'auteur"}`
- **Description** : Ajoute un livre dans la collection
- **Commande `curl`** : curl -X POST http://127.0.0.1:5000/books -H "Content-Type: application/json" -d "{\"title\": \"Titre du Livre\", \"author\": \"Nom de l'Auteur\"}"

### 4. Mettre à jour un livre existant
- **URL** : `/books/<book_id>`
- **Méthode** : `PUT`
- **Headers** : `Content-Type: application/json`
- **Paramètres** : `book_id` : ID du livre à récupérer.
- **Body** : `{"title": "Titre mis à jour", "author": "Auteur mis à jour"}`
- **Description** : Met à jour les informations d'un livre existant.
- **Commande `curl`** : curl -X PUT http://127.0.0.1:5000/books/1 -H "Content-Type: application/json" -d "{\"title\": \"Titre mis à jour\", \"author\": \"Auteur mis à jour\"}"

### 5. Supprimer un livre
- **URL** : `/books/<book_id>`
- **Méthode** : `DELETE`
- **Paramètres** : `book_id` : ID du livre à récupérer.
- **Description** : Supprime un livre de la collection.
- **Commande `curl`** : curl -X DELETE http://127.0.0.1:5000/books/1



