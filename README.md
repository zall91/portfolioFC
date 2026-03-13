# Portfolio BTS SIO SISR — 100% Gratuit (GitHub Pages)

## Structure
```
📁 portfolio/
├── index.html          ← Page du portfolio (chargement dynamique)
├── admin/
│   └── index.html      ← Panneau d'administration
├── data/
│   └── content.json    ← Tout le contenu du site (modifié via l'admin)
└── img/                ← Dossier pour les images
```

## Mise en ligne (5 minutes)

### 1. Créer le dépôt GitHub
1. Va sur [github.com/new](https://github.com/new)
2. Nom du dépôt : `portfolioFC` (ou ce que tu veux)
3. **Public** : obligatoire pour GitHub Pages gratuit
4. Coche "Add a README file"
5. Crée le dépôt

### 2. Uploader les fichiers
1. Sur la page du dépôt, clique sur **Add file** → **Upload files**
2. Glisse-dépose TOUS les fichiers et dossiers de ce zip
3. Clique **Commit changes**

### 3. Activer GitHub Pages
1. Va dans **Settings** → **Pages** (menu de gauche)
2. Source : **Deploy from a branch**
3. Branch : `main` / dossier `/ (root)`
4. Clique **Save**
5. Attends 1-2 minutes, ton site sera sur : `https://ton-pseudo.github.io/portfolioFC/`

### 4. Créer un Token GitHub (pour l'admin)
1. Va sur [github.com/settings/tokens?type=beta](https://github.com/settings/tokens?type=beta)
2. Clique **Generate new token** → **Fine-grained token**
3. Nom : `admin-portfolio`
4. Expiration : 90 jours
5. Repository access → **Only select repositories** → choisis ton dépôt
6. Permissions → Repository permissions → **Contents** → **Read and write**
7. Clique **Generate token** et copie-le

### 5. Se connecter à l'admin
1. Va sur `https://ton-pseudo.github.io/portfolioFC/admin/`
2. Entre le nom du dépôt : `ton-pseudo/portfolioFC`
3. Colle ton token
4. C'est parti ! Tu peux modifier tout le contenu du site.

## Comment ça marche ?

- Tout le contenu est dans **un seul fichier** : `data/content.json`
- Le site (`index.html`) lit ce fichier et affiche le contenu
- L'admin (`admin/index.html`) modifie ce fichier via l'API GitHub
- GitHub Pages re-déploie automatiquement (délai ~1 min après chaque modif)

## Coûts

| Service | Coût |
|---------|------|
| GitHub Pages (hébergement) | **Gratuit** |
| GitHub API (admin) | **Gratuit** (5000 requêtes/heure avec token) |
| Domaine `pseudo.github.io` | **Gratuit** |
| HTTPS | **Gratuit** (automatique) |
| **Total** | **0 €** |

## FAQ

**Q: Mon token expire dans 90 jours, c'est grave ?**
Non, tu en recrées un en 30 secondes sur GitHub. C'est une bonne pratique de sécurité.

**Q: Quelqu'un peut-il accéder à mon admin ?**
Non. Le token est stocké en `sessionStorage` (disparaît quand tu fermes l'onglet). Sans token, impossible de modifier quoi que ce soit.

**Q: Je peux ajouter un nom de domaine personnalisé ?**
Oui ! Dans Settings → Pages → Custom domain. Un `.fr` coûte ~10€/an chez OVH.

**Q: Comment ajouter un formulaire de contact fonctionnel ?**
Crée un compte gratuit sur [formspree.io](https://formspree.io) et remplace la fonction `sendForm()` dans `index.html`.
