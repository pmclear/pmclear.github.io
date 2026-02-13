# Guide : Ajouter des photos à la galerie

## C'est très simple !

La galerie est **automatique**. Vous n'avez pas besoin de modifier le code HTML.

## Structure

Dans le dossier `images/`, créez un sous-dossier pour chaque **sujet** :

```
images/
  ├── La_vie_sur_leau/
  │   ├── Le_cabanon.jpeg
  │   └── Autre_photo.jpeg
  │
  └── Letang/
      ├── Letang.jpeg
      └── Un_peu_dhiver.mov
```

## Ajouter une photo dans un sujet existant

1. Ouvrez le dossier du sujet (ex: `images/La_vie_sur_leau/`)
2. Copiez votre photo dedans
3. Lancez `build`
4. Lancez `deploy`
5. C'est en ligne ! 🎉

## Créer un nouveau sujet

1. Dans `images/`, créez un nouveau dossier (ex: `Ma_famille`)
2. Ajoutez vos photos dans ce dossier
3. Lancez `build`
4. Lancez `deploy`
5. Le nouveau sujet apparaît automatiquement ! 🎉

## Conseils pour les noms

- **Dossiers** : utilisez des underscores `_` au lieu d'espaces
  - `La_vie_sur_leau` s'affichera comme "La vie sur l'eau"
  - `Mes_voyages` s'affichera comme "Mes voyages"

- **Photos** : le nom du fichier devient le titre
  - `Le_cabanon.jpeg` s'affichera comme "Le cabanon"
  - `Coucher_de_soleil.jpeg` s'affichera comme "Coucher de soleil"

## Formats supportés

- **Photos** : .jpeg, .jpg, .png, .gif
- **Vidéos** : .mov, .mp4, .webm

## Important

Le script `build` scanne automatiquement tous les sous-dossiers d'`images/` et génère la galerie. Vous n'avez jamais besoin de modifier `galerie.html` manuellement !
