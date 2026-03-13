# Portfolio BTS SIO SISR — François CAMON

## Structure du projet

```
📁 portfolio/
├── index.html          ← Page principale du portfolio
├── admin/
│   ├── index.html      ← Interface Decap CMS
│   └── config.yml      ← Configuration du CMS
├── img/                ← Dossier pour les images
├── projets/            ← Fichiers Markdown (créés via l'admin)
├── parcours/           ← Fichiers Markdown (créés via l'admin)
└── veille/             ← Fichiers Markdown (créés via l'admin)
```

## Mise en ligne

### 1. GitHub
1. Crée un dépôt public nommé `portfolioFC` (ou autre)
2. Uploade **tous** ces fichiers à la racine du dépôt
3. Assure-toi que le dépôt est **Public**

### 2. Netlify
1. Va sur [netlify.com](https://netlify.com) et connecte-toi avec GitHub
2. Clique sur **Add new site** → **Import an existing project**
3. Sélectionne ton dépôt GitHub
4. Déploie (aucune config spéciale nécessaire)
5. Change le nom du site dans **Site configuration** → **Change site name**

### 3. Admin (Decap CMS)
1. Dans Netlify : **Integrations** → **Identity** → **Enable**
2. Dans **Identity** → **Services** → Active **Git Gateway**
3. Dans **Identity** → **Invite users** → entre ton email
4. Confirme via le mail reçu
5. Va sur `ton-site.netlify.app/admin/` et connecte-toi

## Personnalisation

### Ce que tu dois modifier dans `index.html` :
- **Ton nom** : déjà "François CAMON", à vérifier
- **Parcours** : remplace les exemples par tes vrais diplômes/stages
- **Projets** : remplace par tes vrais projets PPE/TP
- **Veille** : remplace par tes vrais sujets + liens sources
- **Contact** : ajoute ton vrai email et ville
- **Formspree** : crée un compte gratuit sur [formspree.io](https://formspree.io) et remplace le `TODO` dans le code par ton endpoint

### Ajouter un nouveau projet (2 méthodes) :
1. **Via l'admin** : ton-site.netlify.app/admin/ → Nouveau projet
2. **Dans le code** : copie-colle un bloc `project-card` + sa modale dans `index.html`

## Technologies utilisées
- HTML5 / CSS3 (custom, pas de framework lourd)
- AOS.js (animations au scroll)
- Google Fonts (Outfit + JetBrains Mono)
- Decap CMS + Netlify Identity (administration)
