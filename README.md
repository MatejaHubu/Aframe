# Aframe

# README – Scène A-Frame « Springfield »

Cette scène A-Frame met en place un environnement 3D interactif inspiré de Springfield, avec des modèles GLB, des animations, du son et de la vidéo, directement depuis un simple fichier HTML. :contentReference[oaicite:0]{index=0}

## Structure générale

- Utilisation d’A-Frame 1.6.0 et de quelques composants complémentaires :
  - `aframe-extras` (animations, helpers)
  - `aframe-super-hands` (interactions)
  - `aframe-event-set-component`
- Deux composants personnalisés gèrent les nuages :
  - `cloud` : génère un nuage à partir de plusieurs sphères blanches
  - `cloud-move` : anime les nuages de gauche à droite

## Environnement

- Ciel panoramique avec `<a-sky>`.
- Sol d’herbe et route texturés (maps de couleur, normal, roughness, AO, répétition des textures).
- Ligne jaune au centre de la route pour un rendu « route américaine ».

## Modèles 3D (GLB)

La scène charge différents modèles GLB placés dans le dossier `models/` :

- Personnages : Homer, Bart, Chef Wiggum, Delphox, Itachi, zombie, Transformers.
- Décors : maison des Simpson, maison américaine, étang cartoon, cathédrale de Cologne.
- Objets : voiture (Porsche 911), OVNI, etc.
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
- le tout dans une seule page HTML, exécutable dans un navigateur via un simple serveur web.

