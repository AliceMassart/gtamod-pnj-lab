# GTA MOD : The PNJ Lab

Laboratoire d'expérimentation sur les PNJ (comportements, animations, interactions).

## Fonctionnalités

Commande `gather` :

- `gather` : téléporte les PNJ sur le joueur
- `gather walk` : les fait marcher jusqu'au joueur
- `gather tp waypoint` : les téléporte sur le repère posé sur la carte
- `gather walk 215 -810 0` : les fait marcher jusqu'à des coordonnées précises
- `gather follow` : active/désactive le suivi continu du joueur (tant que c'est activé, les PNJ suivent le joueur où qu'il aille) ; donner un ordre de destination explicite désactive automatiquement le suivi

Si la ressource `foule_throttle` est démarrée et a une foule de spawnée, ces ordres s'appliquent à la foule entière, quel que soit son effectif (10, 300, 1000...). Sinon, ils s'appliquent aux PNJ ambiants chargés autour du joueur.

Un nouvel ordre remplace toujours proprement le précédent, même s'il est encore en train de s'appliquer (changement de direction en cours de route, ordres donnés à la suite sans bug).

## Prérequis

- Serveur FiveM à jour
- (Optionnel) Le mod `foule-throttle` démarré avant, pour cibler sa foule en plus des PNJ ambiants

## Installation

1. Télécharger le dossier `pnj_lab`
2. Copier le dossier `pnj_lab` dans `resources/`
3. Ajouter `ensure pnj_lab` dans ton `server.cfg`
4. Redémarrer le serveur

## Structure du dossier

```
gtamod-pnj-lab/
├─ pnj_lab/                 -- dossier du mod
│  ├─ client.lua            -- script principal (commande /gather)
│  └─ fxmanifest.lua
└─ README.md
```

## Crédits

Tuto et mod réalisés par :
Alice MASSART, PAD EMD 2026.
