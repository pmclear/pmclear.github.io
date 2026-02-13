# 📝 Comment ajouter des articles à votre blog

## Méthode simple en 3 étapes

### ✅ ÉTAPE 1 : Créer votre article

**1. Dupliquez le fichier modèle :**
```
blog/articles/TEMPLATE-ARTICLE.html
```

**2. Renommez-le :**
- Exemple : `mon-nouvel-article.html`
- Utilisez des tirets `-` au lieu d'espaces
- Pas de caractères spéciaux

**3. Ouvrez-le et modifiez :**
- Le titre (`<title>` et `<h1>`)
- La date
- Le contenu (les paragraphes `<p>`)
- Ajoutez des photos si vous voulez

---

### ✅ ÉTAPE 2 : Ajouter l'article sur la page d'accueil

**1. Ouvrez `blog/index.html`**

**2. Cherchez la section "Articles récents"**

**3. Copiez ce bloc et personnalisez-le :**

```html
<article class="article-card">
    <div class="article-image">
        <img src="images/votre-photo.jpg" alt="Description">
    </div>
    <div class="article-content">
        <h3>Titre de votre article</h3>
        <p class="article-date">12 février 2026</p>
        <p class="article-excerpt">
            Un court résumé de votre article en 1-2 phrases...
        </p>
        <a href="articles/mon-nouvel-article.html" class="read-more">Lire la suite →</a>
    </div>
</article>
```

**4. Collez-le AVANT les autres articles** (pour qu'il apparaisse en premier)

---

### ✅ ÉTAPE 3 : Déployer

```bash
deploy
```

Puis glissez-déposez sur Netlify !

---

## 🎨 Variantes d'articles

### Article avec photo :
```html
<article class="article-card">
    <div class="article-image">
        <img src="images/ma-photo.jpg" alt="Ma photo">
    </div>
    <div class="article-content">
        <h3>Mon titre</h3>
        <p class="article-date">Date</p>
        <p class="article-excerpt">Résumé...</p>
        <a href="articles/mon-article.html" class="read-more">Lire la suite →</a>
    </div>
</article>
```

### Article sans photo :
```html
<article class="article-card">
    <div class="article-content">
        <h3>✨ Mon titre</h3>
        <p class="article-date">Date</p>
        <p class="article-excerpt">Résumé...</p>
        <a href="articles/mon-article.html" class="read-more">Lire la suite →</a>
    </div>
</article>
```

---

## 💡 Astuces

**Pour ajouter des émojis dans les titres :**
- ✨ Copier-coller depuis https://emojipedia.org/
- Ou utiliser Ctrl + Cmd + Espace sur Mac

**Pour formater le texte dans l'article :**
- `<strong>texte en gras</strong>`
- `<em>texte en italique</em>`
- `<h2>Sous-titre</h2>`

**Pour ajouter plusieurs photos :**
Répétez juste la ligne :
```html
<img src="../images/photo1.jpg" alt="Photo 1">
<img src="../images/photo2.jpg" alt="Photo 2">
```

---

## 📋 Checklist

Avant de déployer :

- [ ] Article créé dans `blog/articles/`
- [ ] Titre et contenu modifiés
- [ ] Photos ajoutées dans `blog/images/` (si besoin)
- [ ] Article ajouté dans `index.html`
- [ ] Testé en local : http://localhost:8000
- [ ] Lancé `deploy`
- [ ] Glissé-déposé sur Netlify

---

## 🎯 Exemple complet

**Fichier :** `blog/articles/ma-reflexion.html`

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Ma réflexion du jour - ClearVision</title>
    <link rel="stylesheet" href="../styles.css">
    <!-- ... styles ... -->
</head>
<body>
    <header>
        <h1>ClearVision</h1>
        <p class="subtitle">Bienvenue sur mon espace personnel</p>
    </header>

    <main>
        <article class="article-full">
            <h1>Ma réflexion du jour</h1>
            <span class="date">12 février 2026</span>

            <p>Aujourd'hui, j'ai réfléchi à...</p>
            <p>Cette expérience m'a appris que...</p>

            <a href="../index.html" class="back-link">← Retour</a>
        </article>
    </main>

    <footer>
        <p>&copy; 2026 ClearVision</p>
    </footer>
</body>
</html>
```

**Dans `index.html` :**

```html
<article class="article-card">
    <div class="article-content">
        <h3>💭 Ma réflexion du jour</h3>
        <p class="article-date">12 février 2026</p>
        <p class="article-excerpt">
            Quelques pensées sur mon expérience d'aujourd'hui...
        </p>
        <a href="articles/ma-reflexion.html" class="read-more">Lire la suite →</a>
    </div>
</article>
```

---

C'est aussi simple que ça ! 🎉
