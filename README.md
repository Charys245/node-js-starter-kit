# 🚀 Node.js Starter Kit

![Node.js](https://img.shields.io/badge/Node.js-18.x-green)
![Express](https://img.shields.io/badge/Express-4.x-lightgrey)
![MongoDB](https://img.shields.io/badge/MongoDB-6.x-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

Un starter kit moderne et prêt à l'emploi pour démarrer rapidement vos projets **Node.js/Express**. Conçu pour être à la fois **pédagogique** et **professionnel**, il intègre les bonnes pratiques que j'ai acquises lors de ma certification.

---

## ✨ Pourquoi ce starter kit ?

- **⏱️ Gain de temps** : Ne partez pas de zéro, tout est déjà configuré
- **📚 Pédagogique** : Code commenté pour comprendre chaque concept
- **🔧 Maintenable** : Architecture MVC propre et évolutive
- **🔐 Sécurisé** : Authentification JWT, mots de passe hashés, variables d'environnement

---

## 🛠️ Stack technique

| Technologie | Utilisation |
|:------------|:------------|
| **Node.js** | Runtime JavaScript |
| **Express.js** | Framework web |
| **MongoDB** | Base de données NoSQL |
| **Mongoose** | ODM pour MongoDB |
| **JWT** | Authentification |
| **bcrypt** | Hash des mots de passe |
| **dotenv** | Gestion des variables d'environnement |

---

## 📋 Prérequis

- Node.js (version 18 ou supérieure)
- MongoDB (installé en local ou utilisez [MongoDB Atlas](https://www.mongodb.com/atlas))
- npm ou yarn
- Postman (pour tester l'API)

---

## 🚦 Installation en 30 secondes
```bash
# 1. Cloner le repository
git clone https://github.com/Charys245/node-js-starter-kit.git

# 2. Entrer dans le dossier
cd node-js-starter-kit

# 3. Installer les dépendances
npm install

# 4. Configurer les variables d'environnement
cp .env.example .env

# 5. Lancer le serveur
npm run dev
```

Le serveur démarrera sur **http://localhost:3000** 🎉

---

## 📁 Structure du projet
```
node-js-starter-kit/
├── 📂 config/
│   └── db.js              # Configuration et connexion MongoDB
├── 📂 controllers/
│   ├── authController.js   # Logique d'authentification
│   └── userController.js   # CRUD utilisateurs
├── 📂 middleware/
│   ├── auth.js            # Vérification du token JWT
│   └── errorHandler.js    # Gestion centralisée des erreurs
├── 📂 models/
│   └── User.js            # Modèle utilisateur (Mongoose)
├── 📂 routes/
│   ├── authRoutes.js      # Routes d'authentification
│   └── userRoutes.js      # Routes utilisateurs
├── 📂 utils/
│   └── generateToken.js   # Fonction de génération JWT
├── .env.example            # Template des variables d'environnement
├── .gitignore
├── package.json
├── README.md
└── server.js              # Point d'entrée de l'application
```

---

## 🔥 Fonctionnalités incluses

### 1. Authentification complète
- ✅ Inscription avec email/mot de passe
- ✅ Connexion avec génération de token JWT
- ✅ Protection des routes avec middleware
- ✅ Hash des mots de passe (bcrypt)

### 2. API RESTful
- ✅ Routes CRUD pour les utilisateurs
- ✅ Gestion des erreurs
- ✅ Réponses JSON standardisées
- ✅ Validation des données

### 3. Base de données
- ✅ Connexion MongoDB avec Mongoose
- ✅ Modèles avec validation
- ✅ Gestion des erreurs de connexion

### 4. Sécurité
- ✅ Variables d'environnement (.env)
- ✅ Headers sécurisés (cors configuré)
- ✅ Mots de passe hashés
- ✅ Tokens JWT

---

## 📡 API Endpoints

| Méthode | Route | Description | Auth requise |
|:--------|:------|:------------|:------------:|
| POST | `/api/auth/register` | Inscription | ❌ Non |
| POST | `/api/auth/login` | Connexion | ❌ Non |
| GET | `/api/users` | Liste tous les utilisateurs | ✅ Oui |
| GET | `/api/users/:id` | Récupère un utilisateur | ✅ Oui |
| PUT | `/api/users/:id` | Modifie un utilisateur | ✅ Oui |
| DELETE | `/api/users/:id` | Supprime un utilisateur | ✅ Oui |

---

## 🧪 Tester l'API avec Postman

1. Importez la collection Postman (fichier `postman-collection.json` à la racine)
2. Créez un environnement avec la variable `{{base_url}}` = `http://localhost:3000`
3. Testez les routes dans cet ordre :
   - `POST /api/auth/register` pour créer un compte
   - `POST /api/auth/login` pour récupérer un token
   - Copiez le token dans l'en-tête `Authorization: Bearer <token>`
   - Testez les routes protégées

---

## 🔧 Personnalisation

### Variables d'environnement (`.env`)
```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/ma_base_de_donnees
JWT_SECRET=ma_super_cle_secrete_123
JWT_EXPIRE=7d
NODE_ENV=development
```

### Ajouter un nouveau modèle

1. Créez un fichier dans `models/`
2. Définissez le schéma Mongoose
3. Créez le contrôleur associé
4. Ajoutez les routes dans `routes/`

---

## 🤔 Comment utiliser ce kit pour apprendre ?

- **Étape 1** : Faites fonctionner le projet (suivez l'installation)
- **Étape 2** : Testez toutes les routes avec Postman
- **Étape 3** : Lisez les commentaires dans chaque fichier
- **Étape 4** : Modifiez quelque chose (ajoutez un champ au modèle User)
- **Étape 5** : Créez votre propre fonctionnalité (ex: modèle "Article")

---

## 🚀 Prochaines améliorations prévues

- [ ] Tests unitaires avec Jest
- [ ] Documentation Swagger/OpenAPI
- [ ] Rate limiting
- [ ] Refresh tokens
- [ ] Upload de fichiers
- [ ] Validation avec Joi

---

## 🤝 Contribuer

Les contributions sont les bienvenues ! Que ce soit pour :

- 🐛 Signaler un bug
- 💡 Suggérer une amélioration
- 📚 Améliorer la documentation
- ✨ Proposer une nouvelle fonctionnalité

---

## 📄 Licence

Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 🙏 Remerciements

Ce projet a été créé dans un but d'apprentissage, suite à l'obtention de ma certification Node.js/Express. J'espère qu'il vous sera aussi utile qu'à moi !

---

⭐ **N'oubliez pas de mettre une étoile si ce projet vous aide !**

👨‍💻 Créé avec ❤️ par [Charys245](https://github.com/Charys245)