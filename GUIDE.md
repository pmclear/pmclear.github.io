# 📖 Guide d'utilisation de votre blog

## 📸 Comment ajouter des photos

### Étape 1 : Mettre vos photos dans le bon dossier

1. Prenez vos photos (depuis votre téléphone, appareil photo, etc.)
2. Glissez-les dans le dossier : `/Users/pmtech/ClaudeProjets/blog/images/`
3. **Renommez-les simplement** :
   - ✅ BON : `vacances-plage.jpg`, `mon-chat.jpg`, `sunset.jpg`
   - ❌ ÉVITEZ : `IMG_1234.jpg`, `Photo 12 mars.jpg` (évitez les espaces)

**Astuce** : Les formats acceptés sont `.jpg`, `.jpeg`, `.png`, `.gif`

---

### Étape 2 : Utiliser vos photos dans un article

Dans votre fichier article HTML, trouvez cette ligne :

```html
<!-- <img src="../images/votre-photo.jpg" alt="Description de la photo"> -->
```

**Décommentez-la** (retirez les `<!--` et `-->`) et remplacez le nom :

```html
<img src="../images/vacances-plage.jpg" alt="Photo de mes vacances à la plage">
```

**Explication** :
- `src="../images/vacances-plage.jpg"` = le chemin vers votre photo
- `alt="..."` = une description (pour l'accessibilité et si l'image ne charge pas)

---

## ✍️ Comment créer un nouvel article

### Méthode simple : Copier-coller

1. **Dupliquez** le fichier `mon-premier-article.html` dans le dossier `articles/`
2. **Renommez-le**, par exemple : `mes-vacances-2026.html`
3. **Ouvrez-le** avec un éditeur de texte (TextEdit, VS Code, etc.)
4. **Modifiez** :
   - Le titre (`<title>` et `<h1>`)
   - La date
   - Le contenu (les paragraphes `<p>`)
   - L'image si vous en ajoutez une

### Étape par étape

**1. Changez le titre de la page (dans le `<head>`) :**
```html
<title>Mes vacances 2026 - Mon Blog</title>
```

**2. Changez le titre visible (dans le `<article>`) :**
```html
<h1>Mes vacances 2026</h1>
```

**3. Changez la date :**
```html
<span class="date">15 février 2026</span>
```

**4. Écrivez votre contenu :**
```html
<p>
    Cette année, je suis parti en vacances à la montagne.
    C'était magnifique !
</p>

<p>
    Voici quelques photos de ce voyage incroyable.
</p>
```

**5. Ajoutez vos photos :**
```html
<img src="../images/montagne-1.jpg" alt="Vue sur les sommets">
<img src="../images/montagne-2.jpg" alt="Coucher de soleil">
```

---

## 🔗 Ajouter votre nouvel article sur la page d'accueil

Une fois votre article créé, il faut l'ajouter à la liste sur `index.html` :

**Ouvrez `index.html` et trouvez la section articles.**

**Copiez-collez ce bloc AVANT l'article existant (pour qu'il apparaisse en premier) :**

```html
<article class="article-card">
    <div class="article-image">
        <img src="images/montagne-1.jpg" alt="Montagne">
    </div>
    <div class="article-content">
        <h3>Mes vacances 2026</h3>
        <p class="article-date">15 février 2026</p>
        <p class="article-excerpt">
            Cette année, direction la montagne pour des vacances
            inoubliables sous la neige !
        </p>
        <a href="articles/mes-vacances-2026.html" class="read-more">Lire la suite →</a>
    </div>
</article>
```

**Personnalisez** :
- L'image (`src="images/..."`)
- Le titre (`<h3>`)
- La date
- Le résumé (texte dans `article-excerpt`)
- Le lien vers votre fichier article

---

## 🎨 Résumé du processus

1. **Pour une photo** → Mettez-la dans `images/`
2. **Pour un article** → Créez un fichier `.html` dans `articles/`
3. **Pour qu'il apparaisse** → Ajoutez-le dans la liste de `index.html`

---

## ⚡ Raccourci mental

Pensez à votre blog comme à un journal :
- **images/** = vos photos en vrac dans une boîte
- **articles/** = les pages de votre journal
- **index.html** = la table des matières

Vous écrivez d'abord la page (l'article), puis vous la référencez dans la table des matières (index.html) !
