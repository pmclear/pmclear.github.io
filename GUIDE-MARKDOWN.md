# 📝 Guide Markdown - Écrire des articles facilement

## Qu'est-ce que Markdown ?

**Markdown** est un format d'écriture ultra-simple qui se transforme automatiquement en HTML.

**L'analogie :** C'est comme écrire un SMS avec quelques symboles pour la mise en forme, au lieu d'apprendre un langage compliqué !

---

## ✍️ Comment créer un article en Markdown

### Étape 1 : Créer votre fichier

1. Allez dans le dossier : `/Users/pmtech/ClaudeProjets/blog/articles/markdown/`
2. Créez un nouveau fichier avec l'extension `.md` : `mes-vacances.md`
3. Ouvrez-le avec un éditeur de texte simple (TextEdit, VS Code, etc.)

### Étape 2 : Écrire votre contenu

Utilisez la syntaxe Markdown ci-dessous :

---

## 📚 Syntaxe Markdown

### Titres

```markdown
# Titre principal (très gros)
## Titre de section (gros)
### Sous-titre (moyen)
```

### Texte en gras et italique

```markdown
**Texte en gras**
*Texte en italique*
***Texte en gras ET italique***
```

### Listes

**Liste à puces :**
```markdown
- Premier élément
- Deuxième élément
- Troisième élément
```

**Liste numérotée :**
```markdown
1. Première étape
2. Deuxième étape
3. Troisième étape
```

### Ajouter des images

```markdown
![Texte alternatif](../images/votre-photo.jpeg)
```

**Exemple :**
```markdown
![Le cabanon](../images/Le_cabanon.jpeg)
```

### Ajouter des liens

```markdown
[Texte du lien](url-ou-chemin)
```

**Exemple :**
```markdown
[Retour à l'accueil](../../index.html)
[Voir la galerie](../../galerie.html)
```

### Ajouter du code

Pour du code en ligne : `` `votre code` ``

Pour un bloc de code :
````markdown
```
Plusieurs lignes
de code ici
```
````

### Citations

```markdown
> Ceci est une citation.
> Elle peut avoir plusieurs lignes.
```

### Ligne de séparation

```markdown
---
```

---

## 🔗 Lier votre article Markdown au blog

### Méthode 1 : Utiliser le convertisseur existant

1. Mettez votre fichier `.md` dans `articles/markdown/`
2. Dupliquez le fichier `article-markdown.html`
3. Renommez-le : `mon-nouvel-article.html`
4. Ouvrez-le et modifiez cette ligne :

```javascript
const response = await fetch('markdown/mon-article.md');
```

Remplacez `mon-article.md` par le nom de votre fichier.

### Méthode 2 : Créer plusieurs articles Markdown

Vous pouvez créer autant de fichiers `.md` que vous voulez dans `articles/markdown/`, puis créer une page HTML pour chacun qui le charge et l'affiche.

---

## 📋 Exemple complet d'article Markdown

```markdown
# Mes vacances à la montagne

**Date :** 15 février 2026

## Un voyage inoubliable

Cette année, je suis parti en vacances à *la montagne*. C'était **magnifique** !

![Vue sur les sommets](../images/montagne.jpeg)

### Ce que j'ai fait

- Randonnée en raquettes
- Ski de fond
- Soirées au coin du feu

### Mes impressions

> "La montagne, c'est vraiment ressourçant. J'y retournerai sans hésiter !"

---

## Les photos

Voici quelques photos de ce voyage :

![Photo 1](../images/montagne-1.jpeg)
![Photo 2](../images/montagne-2.jpeg)

[Retour à l'accueil](../../index.html)
```

---

## 💡 Pourquoi utiliser Markdown ?

### ✅ Avantages

- **Très simple** : Pas besoin de connaître le HTML
- **Rapide** : Vous vous concentrez sur le contenu, pas le code
- **Lisible** : Même sans être converti, on comprend le texte
- **Portable** : Utilisé partout (GitHub, forums, docs, etc.)

### ❌ Limitations

- Moins de contrôle précis sur le design que le HTML
- Nécessite JavaScript pour la conversion automatique

---

## 🎯 Résumé des étapes

1. **Créer** un fichier `.md` dans `articles/markdown/`
2. **Écrire** votre article avec la syntaxe Markdown
3. **Dupliquer** `article-markdown.html` et le renommer
4. **Modifier** le nom du fichier à charger dans le JavaScript
5. **Ajouter** le lien dans `index.html` pour que l'article apparaisse

---

## 🆘 Aide-mémoire rapide

| Syntaxe | Résultat |
|---------|----------|
| `# Titre` | Titre de niveau 1 |
| `## Titre` | Titre de niveau 2 |
| `**gras**` | **gras** |
| `*italique*` | *italique* |
| `[lien](url)` | Lien cliquable |
| `![alt](image.jpg)` | Image |
| `- item` | Liste à puces |
| `1. item` | Liste numérotée |
| `` `code` `` | Code en ligne |

---

Vous voilà prêt à écrire vos articles en Markdown ! 🎉
