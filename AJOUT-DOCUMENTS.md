# Ajout de la section Documents - 11 février 2026

## 📋 Résumé

Ajout d'une nouvelle section **Documents** au blog ClearVision, permettant d'afficher des fichiers PDF organisés par sujets, sur le même principe que la galerie photos.

## ✨ Fonctionnalités ajoutées

### 1. Page Documents automatique
- Nouvelle page `documents.html` générée automatiquement
- Organisation par sujets (comme la galerie)
- Design cohérent avec le reste du blog (blanc, gris, orange)

### 2. Navigation mise à jour
- Bouton "Voir les documents" sur la page d'accueil
- Lien "Documents" dans le menu de toutes les pages
- Accessible depuis n'importe quelle page du site

### 3. Génération automatique dans build.sh
Le script `build.sh` génère maintenant 3 pages automatiquement :
- ✅ Articles (depuis `articles/markdown/`)
- ✅ Galerie (depuis `images/`)
- ✅ **Documents (depuis `pdfs/`)** ← NOUVEAU

## 📁 Structure créée

```
blog/
├── pdfs/                           ← Nouveau dossier
│   ├── Tiny_house/                 ← Organisation par sujet
│   │   └── brochure_maison_helios.pdf
│   └── Patrimoine_de_la_France/
│       └── Les Vaux de Cernay.pdf
├── documents.html                  ← Généré automatiquement
└── documents-template.html         ← Template pour la génération
```

## 🎨 Design

### Style des cartes documents
- Icône 📄 pour chaque PDF
- Titre extrait du nom de fichier (avec espaces automatiques)
- Lien "Ouvrir le document →" qui ouvre le PDF dans un nouvel onglet
- Hover effect pour l'interactivité

### Titres de sujets
- Couleur orange (#dd8c11) comme pour la galerie
- Bordure inférieure pour séparer les sections
- Police Georgia cohérente avec le reste du site

## ⚙️ Fonctionnement technique

### Conversion automatique des noms
- `Tiny_house` → "Tiny house"
- `brochure_maison_helios.pdf` → "brochure maison helios"
- Les underscores `_` sont remplacés par des espaces

### Parcours des sous-dossiers
Le script `build.sh` :
1. Parcourt chaque sous-dossier dans `pdfs/`
2. Crée un titre de sujet pour chaque dossier
3. Liste tous les PDF du dossier sous ce sujet
4. Génère le HTML final dans `documents.html`

### Chemins relatifs
Les liens PDF utilisent le format : `pdfs/[sujet]/[fichier].pdf`

## 🚀 Utilisation

### Ajouter un nouveau sujet de documents

1. **Créer un dossier** dans `blog/pdfs/`
   ```bash
   mkdir blog/pdfs/Nouveau_sujet
   ```

2. **Ajouter des PDF** dans ce dossier
   ```bash
   cp mon-document.pdf blog/pdfs/Nouveau_sujet/
   ```

3. **Lancer le build**
   ```bash
   build
   ```

4. **Déployer**
   ```bash
   deploy
   ```

### Exemple complet

```bash
# Créer un nouveau sujet "Voyages"
mkdir blog/pdfs/Voyages

# Ajouter des PDF
cp itineraire-japon.pdf blog/pdfs/Voyages/
cp guide-tokyo.pdf blog/pdfs/Voyages/

# Générer et déployer
build
deploy
```

## 📝 Fichiers modifiés

### Nouveaux fichiers
- `blog/documents-template.html` - Template pour la génération
- `blog/documents.html` - Page générée (écrasée à chaque build)
- `blog/pdfs/` - Dossier pour les PDF

### Fichiers modifiés
- `build.sh` - Ajout de la génération des documents
- `index.html` - Ajout du bouton "Voir les documents"
- `articles.html` - Ajout du lien "Documents" dans la nav
- `galerie-template.html` - Ajout du lien "Documents" dans la nav

## 🎯 Résultat

### Avant
- Articles ✅
- Galerie photos/vidéos ✅
- Documents ❌

### Après
- Articles ✅
- Galerie photos/vidéos ✅
- **Documents PDF organisés par sujets** ✅

## 📊 Statistiques

- **2 sujets** créés : Tiny house, Patrimoine de la France
- **2 documents** ajoutés
- **4 fichiers** modifiés
- **2 fichiers** créés
- **1 dossier** créé avec sous-dossiers

## 💡 Avantages du système

1. **Automatique** : Tu ajoutes un PDF, tu lances `build`, c'est fait
2. **Organisé** : Les sujets permettent de regrouper les documents
3. **Cohérent** : Même logique que la galerie (facile à comprendre)
4. **Extensible** : Tu peux ajouter autant de sujets que tu veux
5. **Maintenable** : Pas besoin de toucher au HTML, tout est automatique

## 🔄 Workflow complet

```
1. Créer un dossier de sujet dans pdfs/
   ↓
2. Ajouter des PDF dans ce dossier
   ↓
3. Lancer "build"
   → Génère automatiquement documents.html
   ↓
4. Lancer "deploy"
   → Copie tout dans blog-deploy
   ↓
5. Drag & drop sur Netlify
   → C'est en ligne ! 🌐
```

## 🎓 Concept clé

**L'analogie** : La section Documents fonctionne exactement comme la galerie, mais pour les PDF au lieu des photos. Si tu sais utiliser la galerie, tu sais utiliser les documents !

---

*Document créé le 11 février 2026*
*ClearVision - Blog personnel*
