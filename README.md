# Carte 3D du plateau de Paris-Saclay (Processing)

Visualisation interactive en 3D du relief du plateau de Paris-Saclay, avec affichage d'un tracé de randonnée GPX sur le terrain. Le sketch construit un maillage du territoire à partir de données d'altitude, y plaque une texture satellite et permet de naviguer autour de la carte au clavier.

Projet du module IGSD de la Licence Informatique, Université Paris-Saclay, 2020-2021. Réalisé en binôme.

## Fonctionnalités

- Repère 3D (gizmo) et grille de l'espace de travail
- Maillage du terrain à partir d'un fichier d'altitudes et application de la texture
- Affichage d'un tracé GPX en 3D sur le relief
- Caméra orbitale pilotée au clavier et affichage d'informations à l'écran (HUD)

## Commandes

| Touche | Action |
|---|---|
| Flèches haut / bas | Incliner la caméra |
| Flèches gauche / droite | Tourner autour de la carte |
| `+` / `-` | Zoomer / dézoomer |
| `w` | Afficher ou masquer la grille et le terrain |
| `x` | Afficher ou masquer le tracé GPX |

## Lancer le projet

1. Installer [Processing](https://processing.org/download) (version 3 ou supérieure).
2. Ouvrir `MAP_PARIS_SACLAY_3D.pde` : les autres fichiers `.pde` s'ouvrent comme onglets du même sketch.
3. Cliquer sur Exécuter. Le dossier `data/` doit rester à côté du sketch.

## Structure

| Fichier | Rôle |
|---|---|
| `MAP_PARIS_SACLAY_3D.pde` | Point d'entrée : initialisation, boucle d'affichage, gestion du clavier |
| `Workspace.pde` | Grille et repère 3D |
| `Camera.pde` | Caméra orbitale (coordonnées sphériques) |
| `Map3D.pde` | Chargement du relief (RGE ALTI) et conversion entre coordonnées géographiques et 3D |
| `Land.pde` | Maillage et texture du terrain |
| `Gpx.pde` | Lecture et affichage du tracé GPX |
| `Hud.pde` | Informations affichées à l'écran |
| `data/` | Altitudes, texture et tracé |
| `docs/Rapport.pdf` | Rapport du projet |

## Limites connues

Le contrôle de la caméra à la souris n'a pas été finalisé, et la partie visualisation de données est partielle (voir le rapport).

## Auteurs

Ahmed Baaroun, Jessica Imbert
