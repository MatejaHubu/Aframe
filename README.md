# Aframe

# README – Scène A-Frame « Springfield »

Cette scène A-Frame met en place un environnement 3D interactif inspiré de Springfield, avec des modèles GLB, des animations, du son et de la vidéo, directement depuis un simple fichier HTML.

## Structure générale

- Utilisation d’A-Frame 1.6.0 et de quelques composants complémentaires :
  - `aframe-extras` (animations, helpers)
  - `aframe-super-hands` (interactions)
  - `aframe-event-set-component`
- Deux composants personnalisés gèrent les nuages :
  - `cloud` : génère un nuage à partir de plusieurs sphères blanches
  - `cloud-move` : anime les nuages de gauche à droite

## Environnement

- **Ciel** : une image panoramique **360°** appliquée à un `<a-sky>`, donnant l’illusion d’un environnement immersif autour du joueur.
- **Sol en herbe** : un grand plan texturé avec **une texture d’herbe importée** (grass_color, normal, roughness, AO).  
  La texture est répétée pour éviter les effets de flou ou de mosaïque.
- **Route** : second plan texturé (asphalte PBR) avec une ligne jaune au centre pour rappeler une route américaine.
- **Nuages** : entités générées avec `cloud` et animées avec `cloud-move` pour donner de la vie au ciel.

## Modèles 3D (GLB)

La scène charge différents modèles GLB placés dans le dossier `models/` :

- Personnages : Homer, Bart, Chef Wiggum, Delphox, Itachi, Zombie, Transformers.
- Décors : maison des Simpson, maison américaine, étang cartoon, cathédrale de Cologne.
- Objets : voiture (Porsche 911), OVNI, etc.
- Sur la façade de la **maison jaune**, un **poster de Bart** est affiché grâce à un `<a-plane>` texturé, ce qui ajoute un détail visuel lié à l’univers des Simpson.
- Certains modèles sont animés via `animation-mixer` (boucle d’animation).

## Interactions

- **Son D’OH de Homer** :
  - Un `<a-sound>` est attaché à Homer.
  - Clic sur Homer ou sur les textes « PLAY » / « STOP » déclenche ou arrête le son.

- **Vidéo** :
  - La vidéo est déclarée dans `<a-assets>` puis affichée sur un `<a-plane>`.
  - Deux textes cliquables « PLAY » et « STOP » contrôlent la lecture avec `video.play()` / `video.pause()`.

- **Objet interactif (box)** :
  - Une `<a-box>` rouge grossit à chaque clic jusqu’à une taille maximale, puis revient à sa taille d’origine.

- **Déplacement d’objets** :
  - Le composant custom `drag-move` permet de déplacer certains modèles en fonction de la position de la souris.

- **Raycaster souris** :
  - Un curseur avec `cursor="rayOrigin: mouse"` + `raycaster="objects: .clickable"` permet de cliquer les éléments portant la classe `.clickable`.

## Contrôles utilisateur

- Déplacement dans la scène : touches **Z / Q / S / D**.
- Orientation de la vue : **souris**.
- Clic souris : interaction avec les éléments cliquables (son, vidéo, box, modèles 3D).

## Résumé

Cette scène illustre l’utilisation d’A-Frame pour créer un environnement 3D interactif complet :
- gestion d’assets (GLB, textures, son, vidéo),
- composants personnalisés en JavaScript,
- interactions riches (clic, déplacement d’objets, contrôle média),
- décor immersif avec ciel 360° et détails visuels (comme le poster de Bart sur la maison jaune),

- le tout dans une seule page HTML, exécutable dans un navigateur via un simple serveur web.

