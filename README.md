# Reference View Align

Addon Blender pour importer et organiser des **images de référence (blueprints)** sans perdre de temps.
Glisse une image dans la vue 3D : elle est alignée sur la vue, renommée, rangée dans une collection et écartée du modèle, automatiquement.

> Compatible Blender 2.90 et plus (développé et utilisé sur Blender 4.5 LTS).

## Fonctionnalités

### Import automatique
- **Alignement sur la vue active** lors du glisser-déposer ou de *Ajouter > Image > Référence*.
- **Renommage** avec le nom anglais de la vue : `Front`, `Back`, `Left`, `Right`, `Top`, `Bottom` (ou `User` / `Camera`). Option pour garder le nom de l'image (`Front_photo`).
- **Placement au curseur 3D**, avec sélecteurs **X / Y / Z** pour choisir les axes.
- **Rangement automatique** dans la collection `blueprint` (créée si elle n'existe pas, nom modifiable).
- **Réglages d'affichage par défaut** : opacité, profondeur (par défaut / devant / derrière), visibilité en perspective et en orthographique.
- **Écartement selon la vue** : distance réglable (6 m par défaut) et axe au choix pour chaque paire de vues (Face/Arrière, Droite/Gauche, Dessus/Dessous). Les vues inverses (Ctrl + pavé numérique) prennent la distance en négatif.

### Mode Auto / Manuel
- **Auto** : les réglages d'affichage et la distance du slider sont appliqués **en direct à toutes les images de la collection**.
- **Manuel** : réglages image par image, les réglages globaux sont grisés.

### Vues précises
- Six boutons (Face, Arrière, Droite, Gauche, Dessus, Dessous) pour orienter les images sur une vue donnée.
- Le bouton devient **bleu** si une image de cette vue existe déjà dans la collection. Il bascule alors seulement la vue 3D sans toucher aux images (**Ctrl + clic** pour forcer la mise à jour).

### Masquer / afficher par vue
- Boutons en haut du panneau pour masquer ou ré-afficher en un clic les images Face, Arrière, Dessous, Dessus, Gauche ou Droite.

### Cube ref
- Cube de référence avec point zéro : **bas du cube sur Z**, **centré sur X**, **face à Y = 0**.
- Taille réglable, affichage fil de fer, position X / Y / Z saisissable.
- Slider de déplacement **selon la vue active** (mêmes axes que l'écartement des images).
- Rangé dans sa propre collection `cube ref`.

### Divers
- Indicateur de **vue active** (Face, Droite, Dessus, Vue libre, Caméra…) et bouton Actualiser.
- Sélecteur de cible : sélection ou toutes les références.
- Entrées dans le menu **Objet** de la vue 3D.

## Installation

1. Télécharge `reference_view_align.zip` depuis la page [Releases](../../releases).
2. Dans Blender : **Édition > Préférences > Add-ons > Installer…** puis choisis le zip.
3. Coche l'addon **Reference View Align**.
4. Ouvre la vue 3D, appuie sur **N** et va dans l'onglet **Référence**.

> En cas de mise à jour, ferme Blender et supprime l'ancien dossier de l'addon avant de réinstaller.

## Utilisation rapide

1. Place-toi dans la vue voulue (ex. pavé numérique `1` pour la vue de face).
2. Glisse ton image dans la vue 3D.
3. L'image est alignée, renommée, écartée et rangée dans `blueprint`.
4. Ajuste la distance avec le slider : toutes les images de la collection suivent.

## Limites connues
- L'alignement automatique utilise la dernière vue 3D affichée si plusieurs vues sont ouvertes.
- L'écartement en direct ne concerne que les images orientées dans l'une des six vues standards.
