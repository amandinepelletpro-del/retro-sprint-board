# 🔁 Retro Board — Et si on recommençait ce sprint ?

Board de rétrospective collaboratif en temps réel.  
Construit avec React + Firebase Firestore + déployable sur Vercel.

---

## 🚀 Démarrage rapide

### 1. Cloner le projet

```bash
git clone https://github.com/TON_USERNAME/retro-board.git
cd retro-board
npm install
```

### 2. Configurer Firebase

1. Va sur [console.firebase.google.com](https://console.firebase.google.com)
2. Crée un projet > enregistre une Web App
3. Active **Firestore Database** (mode test)
4. Copie le fichier `.env.example` en `.env` :

```bash
cp .env.example .env
```

5. Remplis les valeurs dans `.env` avec ta config Firebase

### 3. Lancer en local

```bash
npm start
```

L'app tourne sur [http://localhost:3000](http://localhost:3000)

---

## 🌍 Déployer sur Vercel

### Option A — Via l'interface Vercel (recommandé)

1. Pousse le projet sur GitHub
2. Va sur [vercel.com](https://vercel.com) > **New Project** > importe ton repo GitHub
3. Dans **Environment Variables**, ajoute chaque variable de ton `.env`
4. Clique **Deploy** — Vercel te génère une URL publique

### Option B — Via le terminal

```bash
npx vercel login
npx vercel --prod
```

> ⚠️ Pense à configurer les variables d'environnement dans le dashboard Vercel  
> (Settings > Environment Variables) avant de déployer.

---

## 🗂 Structure du projet

```
retro-board/
├── public/
│   └── index.html
├── src/
│   ├── App.js          # Composant principal + logique Firebase
│   ├── firebase.js     # Initialisation Firebase (lit les variables .env)
│   └── index.js        # Point d'entrée React
├── .env.example        # Template des variables d'environnement
├── .gitignore          # Exclut .env et node_modules de Git
├── vercel.json         # Config routing pour Vercel
└── package.json
```

---

## 🔄 Changer de board à chaque sprint

Dans `src/App.js`, ligne 10, modifie la constante `BOARD_ID` :

```js
const BOARD_ID = "sprint-43"; // ← change le numéro à chaque sprint
```

Chaque valeur crée un board isolé avec ses propres données dans Firestore.

---

## 🛠 Stack technique

| Technologie | Usage |
|-------------|-------|
| React 18 | Interface utilisateur |
| Firebase Firestore | Base de données temps réel |
| Vercel | Hébergement & déploiement |

---

## 📄 Licence

MIT — libre d'utilisation et de modification.
