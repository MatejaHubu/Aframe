# Aframe

README — Scène A-Frame « Springfield »
🎯 Objectif

Cette scène A-Frame représente un environnement 3D interactif inspiré de Springfield.
Elle intègre des modèles GLB, des animations, des interactions utilisateur, du son, de la vidéo et plusieurs composants personnalisés.
L’objectif est de démontrer la capacité à construire une scène interactive en VR Web uniquement en HTML, JavaScript et A-Frame.

🏞️ Composition de la scène
Environnement

Ciel panoramique (a-sky)

Sol texturé (herbe avec normal map, AO, roughness)

Route avec texture PBR et ligne jaune

Nuages générés et animés avec les composants personnalisés :

cloud

cloud-move

🧍‍♂️ Modèles 3D (GLB)

La scène charge plusieurs modèles .glb, dont :

Homer animé (avec son D’OH)

Bart

Chef Wiggum animé

Porsche 911 Turbo S

Deux maisons (Simpsons + maison américaine)

OVNI animé

Transformateur électrique

Delphox animé

Itachi animé

Zombie Homer (shadow.glb)

Cathédrale de Cologne (objet monumental)

Tous ces objets peuvent être déplacés grâce au composant drag-move.

🎛️ Interactions utilisateur
Son

Cliquer sur Homer → joue le son D’OH

Deux boutons : PLAY et STOP gèrent également la lecture

Vidéo

Un écran diffuse une vidéo en boucle

Boutons interactifs :

PLAY → lance la vidéo

STOP → met en pause

Box interactive

Une box rouge grossit à chaque clic

Quand elle atteint la taille max, elle revient à la taille initiale

Raycaster souris

Le curseur (rayOrigin: mouse) permet de cliquer sur tous les éléments .clickable

Déplacement d’objets

Le composant drag-move personnalisé permet de déplacer les modèles simplement en glissant la souris

🧩 Composants personnalisés
cloud

Construit un nuage composé de plusieurs sphères blanches.

cloud-move

Anime chaque nuage horizontalement avec une interpolation douce.

drag-move

Permet de déplacer une entité dans la scène grâce aux mouvements de la souris.

fix-bones

Corrige les problèmes d’ossatures et de skinning sur certains modèles animés.

🎮 Contrôles utilisateur

WASD : déplacement dans la scène

Souris : orientation de la caméra + clic sur les objets

Compatibilité VR via A-Frame et Super-Hands

✔️ Conclusion

Cette scène démontre l’usage des principales fonctionnalités offertes par A-Frame :

Chargement et animation de modèles GLB

Gestion du son et de la vidéo

Interactions avancées (clic, déplacement d’objets, UI 3D)

Création de composants JavaScript personnalisés

Construction d’un environnement 3D cohérent et interactif

Elle illustre la capacité à réaliser une mini-expérience VR complète directement dans un navigateur web.
