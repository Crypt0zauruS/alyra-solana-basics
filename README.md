# Solana React Project 🚀

Bienvenue dans le projet de base Solana React ! Ce projet utilise React pour construire une interface utilisateur interagissant avec la blockchain Solana via des programmes Anchor.

## Structure du Projet 📁

Voici un aperçu des fichiers et dossiers principaux de votre projet :

```plaintext
alyra-react/
├── node_modules/
├── public/
├── src/
│   ├── contract/
│   │   └── lib.rs
│   ├── helpers/
│   │   └── solana.helper.ts
│   ├── idl/
│   │   └── idl.ts
│   ├── pages/
│   │   ├── Account.tsx
│   │   ├── Authentication.tsx
│   │   ├── Dashboard.tsx
│   │   ├── Transfer.tsx
│   │   ├── App.css
│   │   ├── App.tsx
│   │   ├── index.css
│   │   └── index.tsx
├── .dropboxignore
├── .env
├── .gitignore
├── config-overrides.js
├── package-lock.json
├── package.json
├── README.md
└── tsconfig.json
```

## Description des Fichiers 📄

### `src/contract/lib.rs`

Contient le code du programme Solana écrit en Rust utilisant Anchor. Définit une instruction `initialize` qui initialise un compte avec des champs `data` et `age`.

### `src/helpers/solana.helper.ts`

Fonctions utilitaires pour interagir avec la blockchain Solana :

- `getSolanaBalance` : Obtient le solde en SOL d'une adresse donnée.
- `getWalletAuthentication` : Signe un message avec le portefeuille.
- `verifyEncodedMessage` : Vérifie un message signé.
- `getRecentBlockhash` : Obtient le dernier blockhash.
- `transferSolana` : Effectue un transfert de SOL.
- `initializeAccount` : Initialise un compte avec Anchor.
- `getAccount` : Récupère les informations d'un compte.
- `getInitializeAccountTransaction` : Crée une transaction d'initialisation de compte avec Anchor.
- `getInitializeAccountTransactionWWithoutAnchor` : Crée une transaction d'initialisation de compte sans utiliser Anchor.

### `src/idl/idl.ts`

Contient la définition de l'IDL (Interface Definition Language) pour le programme Solana, décrivant les instructions, les comptes et les arguments utilisés par le programme.

### `src/pages/Account.tsx`

Composant React pour afficher et gérer les informations du compte. Permet de récupérer et d'afficher les informations du compte, ainsi que d'initialiser un nouveau compte.

### `src/pages/Authentication.tsx`

Composant React pour l'authentification avec le portefeuille Solana. Permet de signer des messages et de vérifier les signatures avec le portefeuille Solana.

### `src/pages/Dashboard.tsx`

Composant principal qui intègre les différents composants de l'application. Vérifie si le portefeuille est connecté et affiche les composants `Authentication`, `Transfer`, et `Account`.

### `src/pages/Transfer.tsx`

Composant React pour transférer des SOL. Permet de saisir le montant et l'adresse de destination, et d'effectuer un transfert de SOL.

### `src/pages/App.tsx`

Composant principal de l'application React. Affiche le solde en SOL du portefeuille connecté, le bouton de connexion du portefeuille, et le composant `Dashboard`.

### `config-overrides.js`

Fichier de configuration pour remplacer certains paramètres de Webpack. Remplace certains modules de Node.js avec des versions compatibles avec le navigateur et ajoute des polyfills.

### `.env`

Fichier de configuration des variables d'environnement.

### `.gitignore`

Fichier pour ignorer certains fichiers et dossiers dans Git.

### `package-lock.json` et `package.json`

Fichiers de configuration npm, décrivant les dépendances du projet et verrouillant les versions des paquets.

### `README.md`

Fichier de documentation du projet.

### `tsconfig.json`

Fichier de configuration TypeScript, décrivant les options de compilation TypeScript pour le projet.

## Démarrage 🚀

1. **Installation des dépendances** :
   ```
   npm install
   ```
2. **Démarrage du serveur de développement** :
   ```
    npm start
   ```
3. **Ouvrez votre navigateur** :
   Ouvrez [http://localhost:3000](http://localhost:3000) pour voir l'application en action.

4. **Happy coding! 😃**
