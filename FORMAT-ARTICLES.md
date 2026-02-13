# Format des articles Markdown

## Structure d'un article

Chaque article doit commencer par des **métadonnées** entre `---` :

```markdown
---
title: Le titre de votre article
date: 2026-02-12
image: nom-de-photo.jpeg
excerpt: Un court résumé en une phrase
---

# Votre contenu commence ici

Écrivez votre article normalement en Markdown...
```

## Métadonnées disponibles

### Obligatoires :
- `title` : Le titre de votre article
- `excerpt` : Résumé court (1-2 phrases)

### Optionnelles :
- `date` : Date au format YYYY-MM-DD (si absent, date du jour)
- `image` : Nom de la photo dans `images/` (si absent, pas d'image)

## Exemples

### Article avec photo :

```markdown
---
title: Mes vacances à la montagne
date: 2026-02-15
image: montagne.jpeg
excerpt: Un séjour inoubliable dans les Alpes avec de magnifiques paysages.
---

# Mes vacances à la montagne

C'était incroyable ! Les paysages étaient à couper le souffle...

## Ce que j'ai fait

- Randonnée
- Ski
- Détente

![Vue sur les sommets](../../images/montagne.jpeg)
```

### Article sans photo :

```markdown
---
title: Réflexion du jour
date: 2026-02-12
excerpt: Quelques pensées sur la vie et le bonheur.
---

# Réflexion du jour

Aujourd'hui j'ai pensé à...
```

## Syntaxe Markdown

### Titres :
```markdown
# Titre niveau 1
## Titre niveau 2
### Titre niveau 3
```

### Texte :
```markdown
**gras**
*italique*
***gras et italique***
```

### Listes :
```markdown
- Item 1
- Item 2
- Item 3

1. Premier
2. Deuxième
3. Troisième
```

### Images :
```markdown
![Description](../../images/photo.jpeg)
```

### Liens :
```markdown
[Texte du lien](https://example.com)
```

## Workflow

1. Créez votre fichier `.md` dans `articles/markdown/`
2. Ajoutez les métadonnées en haut
3. Écrivez votre article
4. Lancez `build` pour générer le HTML
5. Lancez `deploy` pour mettre en ligne

C'est tout ! 🎉
