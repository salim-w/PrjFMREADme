# PrjFMREADme
# ChatterBox : Application de Messagerie en Temps Réel

## 📖 Description
ChatterBox est une application web permettant aux utilisateurs de communiquer en temps réel via des messages texte. Le projet intègre des fonctionnalités modernes comme l’authentification des utilisateurs et les salles de chat.

## 🔧 Caractéristiques

### 🔑 Authentification des utilisateurs
- **Inscription et connexion** avec un email et un mot de passe.
- **Profil utilisateur** avec un statut (en ligne/hors ligne).

### 🔌 Salles de chat
- **Création de salles** publiques ou privées.
- Possibilité de **rejoindre ou quitter** des salles de discussion.

### 🔒 Messagerie en temps réel
- **Envoi et réception** de messages en temps réel avec des notifications pour les nouveaux messages.
- **Historique des messages** enregistré dans une base de données.

### 🔄 Interface utilisateur intuitive
- **Liste des utilisateurs connectés** dans chaque salle.
- Indicateur **"En train d'écrire..."** pour une meilleure interaction.

### 💪 Fonctionnalités avancées (optionnel)
- **Pièces jointes** : Envoi d’images, fichiers ou emojis.
- **Suppression et modification** de messages.

## ⚡ Impact
- **Favorise la communication** rapide et efficace entre les utilisateurs.
- Utile pour des **communautés**, des **projets scolaires**, ou des **environnements professionnels**.

## 🔧 Architecture Logicielle
L'application est composée de :

- **Backend** : Node.js avec Express.js
- **Frontend** : React.js
- **Base de données** : MongoDB

## 🔍 Prérequis
1. **Git** : Assurez-vous que Git est installé. Sinon, téléchargez-le depuis [git-scm.com](https://git-scm.com).
2. **Node.js** : Installez Node.js depuis [nodejs.org](https://nodejs.org).
3. **MongoDB** : Assurez-vous que MongoDB est installé et fonctionne sur le port par défaut 27017.

## 🛠‟ Installation

### Backend
```bash
cd backend
npm install
npm start
```

### Frontend
```bash
cd frontend
npm install
npm start
```

### Lancer MongoDB
Assurez-vous que le service MongoDB est démarré.

## 🏢 Accès à l'application
- **Frontend** : [http://localhost:3000](http://localhost:3000)
- **Backend API** : [http://localhost:5000](http://localhost:5000)

## 🌐 Fonctionnalités Techniques

### Backend
- **Node.js** avec **Express.js** pour les APIs REST.
- **Socket.IO** pour la messagerie en temps réel.
- **MongoDB** comme base de données.

#### Exemple de dépendances
```json
{
  "dependencies": {
    "express": "^4.18.0",
    "mongoose": "^6.2.0",
    "socket.io": "^4.4.1",
    "bcrypt": "^5.0.1",
    "jsonwebtoken": "^8.5.1"
  }
}
```

### Frontend
- **React.js** pour une interface utilisateur dynamique.
- **Axios** pour les appels API.
- **Socket.IO Client** pour la communication en temps réel.

## 🏠 Docker

### Docker Compose
```yaml
version: '3.8'

services:
  mongodb:
    image: mongo:latest
    ports:
      - "27017:27017"
    volumes:
      - mongodb_data:/data/db

  backend:
    build:
      context: ./backend
    ports:
      - "5000:5000"
    depends_on:
      - mongodb
    environment:
      MONGO_URI: mongodb://mongodb:27017/chatterbox

  frontend:
    build:
      context: ./frontend
    ports:
      - "3000:3000"
    depends_on:
      - backend

volumes:
  mongodb_data:
```

## 👥 Contributeurs
- Abdelbasset Zaggabi
- Collaborateurs bienvenus : [Lien GitHub](https://github.com/ton_projet_chatterbox)

