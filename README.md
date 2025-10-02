# bookshop
Bookshop est conçu pour : ✅ Apprendre les bonnes pratiques (clean code, architecture modulaire). ✅ Maîtriser Prisma et PostgreSQL pour des applications robustes. ✅ Créer un projet professionnel prêt pour la production.

# Bookshop

**Une plateforme moderne de vente de livres en ligne, inspirée de Cultura, construite avec Node.js, Prisma et PostgreSQL.**

---

## 📌 Description du Projet

**Bookshop** est une application web **full-stack** permettant aux utilisateurs d’acheter, vendre et découvrir des livres en ligne. Le projet est conçu pour être **scalable**, **sécurisé** et **maintenable**, en utilisant les technologies modernes du développement JavaScript/TypeScript.

Avec une **architecture modulaire**, Bookshop offre :
- Un **catalogue de livres** avec recherche et filtres avancés.
- Un **système de panier et de paiement** sécurisé (Stripe/PayPal).
- Une **gestion des utilisateurs** (inscription, connexion, profils).
- Un **tableau de bord administrateur** pour gérer les stocks et les commandes.

---

## 🛠 Stack Technique

| Catégorie          | Technologie                                                                 | Rôle                                                                                     |
|--------------------|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| **Backend**        | Node.js (ES Modules)                                                        | Serveur API RESTful/GraphQL, logique métier.                                              |
| **ORM**           | [Prisma](https://www.prisma.io/)                                           | Gestion des modèles de données et interactions avec PostgreSQL.                         |
| **Base de données** | [PostgreSQL](https://www.postgresql.org/)                                  | Stockage des données (livres, utilisateurs, commandes, etc.).                          |
| **Authentification** | JWT (JsonWebToken) + bcryptjs                              | Sécurisation des routes et gestion des sessions utilisateurs.                           |
| **Paiements**     | Stripe API / PayPal API                                                     | Intégration des paiements en ligne.                                                      |
| **Frontend**      | React.js / Next.js (optionnel)                                             | Interface utilisateur dynamique et responsive.                                           |
| **Tests**         | Jest + Supertest                                                           | Tests unitaires, d’intégration et E2E.                                                   |
| **Validation**    | Zod                                                                         | Validation des données côté serveur.                                                    |
| **Logging**       | Winston / Pino                                                              | Journalisation des événements et erreurs.                                               |
| **Déploiement**   | Docker + Kubernetes / Heroku / AWS ECS                                     | Containerisation et déploiement continu.                                                |
| **CI/CD**         | GitHub Actions / GitLab CI                                                  | Automatisation des tests et déploiements.                                               |

---

## 📦 Structure du Projet

```bash
bookshop/
├── src/
│   ├── config/          # Configuration (Prisma, JWT, etc.)
│   ├── controllers/     # Logique métier (classes ES2021+)
│   ├── models/          # Modèles Prisma
│   ├── routes/          # Routes Express
│   ├── services/        # Services métiers (ex: PaymentService)
│   ├── middlewares/     # Middlewares (auth, validation, etc.)
│   ├── utils/           # Utilitaires (logger, errors, etc.)
│   ├── public/          # Fichiers statiques
│   ├── app.js           # Configuration Express
│   └── index.js         # Point d’entrée
├── prisma/
│   ├── schema.prisma    # Schéma Prisma
│   └── migrations/      # Migrations de la base de données
├── .env                # Variables d’environnement
├── .eslintrc.json      # Configuration ESLint
├── package.json
└── README.md
