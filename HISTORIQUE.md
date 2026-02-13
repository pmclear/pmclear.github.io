# Historique des améliorations - ClearVision

## 📅 10 février 2026

### ✨ Améliorations majeures

#### 1. Correction du système de build
- **Problème résolu** : Le fichier `articles.html` était incomplet (manquait structure HTML)
- **Solution** : Recréé la structure complète avec en-tête, navigation, footer
- **Amélioration** : Correction du script `build.sh` pour compatibilité macOS (remplacement de `head -n -1` par `sed '$d'`)

#### 2. Ajout de la vidéo dans la galerie
- **Ajout** : Vidéo "Un peu d'hiver" maintenant visible dans la galerie
- **Support** : Format vidéo avec lecteur intégré (controls)

#### 3. Organisation de la galerie par sujets (AUTOMATIQUE) 🎉
**C'est la grande amélioration du jour !**

##### Avant
- Galerie statique : fallait modifier le HTML manuellement pour chaque photo

##### Après
- **Système automatique** : les sous-dossiers dans `images/` deviennent automatiquement des sujets
- **Structure** :
  ```
  images/
    ├── La_vie_sur_leau/
    │   ├── Le_cabanon.jpeg
    │   └── Un_peu_dhiver.mov
    └── Letang/
        └── Letang.jpeg
  ```

##### Comment ça marche
1. Chaque **sous-dossier** dans `images/` = un **sujet** dans la galerie
2. Les **fichiers** dans le sous-dossier = les **photos/vidéos** de ce sujet
3. Le script `build` scanne automatiquement et génère `galerie.html`

##### Avantages
- ✅ Plus besoin de toucher au code HTML
- ✅ Ajout de photos ultra-simple : créer un dossier, y mettre des photos, lancer `build`
- ✅ Les noms de dossiers avec `_` s'affichent avec des espaces (ex: `La_vie_sur_leau` → "La vie sur l'eau")
- ✅ Support automatique des images ET vidéos

#### 4. Fichiers créés/modifiés

**Nouveaux fichiers :**
- `galerie-template.html` : Template pour la génération automatique de la galerie
- `GUIDE-GALERIE.md` : Guide complet pour ajouter photos et sujets

**Fichiers modifiés :**
- `build.sh` : Ajout de la génération automatique de la galerie
- `galerie.html` : Maintenant généré automatiquement par `build`

---

## 🎯 État actuel du blog

### Structure complète
```
blog/
├── index.html              # Page d'accueil avec 2 boutons
├── articles.html           # Liste des articles (générée par build)
├── galerie.html            # Galerie par sujets (générée par build)
├── styles.css              # Style classique professionnel
│
├── articles/
│   ├── markdown/           # Vos articles en .md
│   │   └── A propos de mon manifeste.md
│   └── [fichiers .html générés automatiquement]
│
└── images/
    ├── La_vie_sur_leau/    # Sujet 1
    │   ├── Le_cabanon.jpeg
    │   └── Un_peu_dhiver.mov
    └── Letang/             # Sujet 2
        └── Letang.jpeg
```

### Commandes essentielles

- **`build`** : Génère les articles ET la galerie automatiquement
- **`deploy`** : Prépare les fichiers pour Netlify

### Workflow complet

#### Pour ajouter un article :
1. Créer un fichier `.md` dans `blog/articles/markdown/`
2. `build`
3. `deploy`
4. Glisser-déposer sur Netlify

#### Pour ajouter des photos :
1. Créer un dossier dans `images/` (ex: `Mes_vacances`)
2. Y mettre vos photos/vidéos
3. `build`
4. `deploy`
5. Glisser-déposer sur Netlify

---

## 📚 Guides disponibles

- **`GUIDE.md`** : Guide général du blog
- **`GUIDE-GALERIE.md`** : Guide spécifique pour la galerie
- **`FORMAT-ARTICLES.md`** : Format des articles Markdown
- **`GUIDE-MARKDOWN.md`** : Syntaxe Markdown

---

## 🚀 Ce qui rend votre blog unique

1. **Double automatisation** : Articles ET galerie générés automatiquement
2. **Aucun code à écrire** : Vous créez des dossiers et des fichiers, le script fait le reste
3. **Design professionnel** : Style classique, élégant, inspiré des blogs professionnels
4. **Léger et rapide** : Images et vidéos optimisées (86% de réduction de taille)
5. **Simple à maintenir** : Deux commandes (`build` + `deploy`), c'est tout !

---

## 💡 Pour la suite

Vous pouvez maintenant :
- Ajouter autant de sujets que vous voulez dans la galerie
- Créer autant d'articles que vous voulez
- Tout est automatique, profitez-en ! 🎉
