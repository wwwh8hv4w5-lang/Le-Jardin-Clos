# Aegis Protocol : Épervier

Simulation de drone **MALE** armé (Medium Altitude Long Endurance) — vous êtes l’**opérateur capteurs** du drone **ÉPERVIER**.

**Version 2.8** · F.S.M Game House

> Ancien dépôt *Le-Jardin-Clos* / *Prairie Orbitale* : le code a été entièrement remplacé par ce jeu de drone (moteur issu de *Naval Strike Simulation* / *Darksea*).

## Jouer

Ouvre `index.html` dans un navigateur récent **avec WebGL2** (Chrome, Edge, Firefox, Safari récents).  
Tout le jeu tient dans ce seul fichier : aucun serveur, aucune installation.

### Mettre le jeu en ligne avec GitHub Pages

1. Les fichiers sont déjà à la racine de ce dépôt.
2. **Settings → Pages** → Source : *Deploy from a branch* → branche `main` → dossier `/ (root)`.
3. Après une minute : `https://wwwh8hv4w5-lang.github.io/Le-Jardin-Clos/`

## Concept

Vous pilotez la **boule optronique** (TV · IR · illumination laser) d’un drone en orbite (~4 500 m).  
L’état-major (**AQUILA**) vous donne des ordres. Vous devez :

1. **Observer** le terrain (routes, villages, convois, civils, forces hostiles)
2. **Identifier** les cibles (zoom fort, centrage, PID)
3. Demander une **autorisation de tir** (règles d’engagement, CDE — dommages collatéraux estimés)
4. **Désigner au laser** et frapper (MAS-L, BGL-250 / BGL-1000, canon selon charge)
5. **Dévier** si des civils entrent dans la zone pendant le vol de la munition

## Missions

| Code | Titre | Ambiance |
|------|--------|----------|
| ÉPERVIER 1 | Vent de sable | Désert, convoi armé, hameau civil interdit de tir |
| ÉPERVIER 2 | Lisière | Danger close, amis au contact, JTAC |
| ÉPERVIER 3 | Médina | Ville dense, marché, CDE stricte |
| ÉPERVIER 4 | Nuit noire | Opération de nuit |
| ÉPERVIER 5 | Fer de lance | Objectif prioritaire / camion d’armes |
| PATROUILLE | Patrouille libre | Mode libre |

Campagne sauvegardée en localStorage (`aegisEpervierCampaign_v1`).

## Commandes principales

| Action | Souris / tactile | Clavier |
|--------|------------------|---------|
| Orienter la boule (slew) | Glisser sur l’image | — |
| Zoomer | Molette / pincer | — |
| Pointer la carte | Toucher la carte | — |
| Sélectionner une cible | Clic / toucher | — |
| Poursuivre (track) | Double-clic | — |
| Identifier | Bouton **IDENTIFIER** | — |
| Laser | Bouton **LASER** | `L` |
| Tir (maintenir) | Bouton **TIR** | — |
| Déviation | Bouton **DÉVIATION** | — |
| Vision TV / IR | Boutons de mode | `V` |
| Pause | — | `Échap` / `P` |

Interface pensée pour desktop et mobile (HUD fire-control, carte 2D, briefings).

## Armement (selon drone / mission)

- **MAS-L** — missile air-sol léger (guidage laser)
- **BGL-250** / **BGL-1000** — bombes guidées laser
- **Canon** rotatif (selon charge)
- Modes : designation laser, caméra munition (autodirecteur), déviation en zone vide

Plusieurs variantes de drone (polyvalent, salve, vision sous canopée, etc.) avec hangar et loadout.

## Technique

- Rendu **WebGL2** (moteur custom issu de Naval Strike 3.1 / protocole Aegis)
- Échelle : 1 unité ≈ 10 m
- Drone en orbite (rayon ~380 u, altitude ~450 u)
- Monde généré par mission (terrain, routes, bâtiments, végétation, IA véhicules / personnes)
- Cycle jour / nuit, météo, vision TV / IR, ombres centrées sur la visée
- Sauvegarde campagne navigateur

## Fichiers

| Fichier | Rôle |
|---------|------|
| `index.html` | Jeu complet (UI + moteur 3D + missions + IA) |
| `README.md` | Ce document |

## Crédits

- **Jeu** : F.S.M Game House  
- **Moteur 3D** : base *Naval Strike Simulation 3.1* / protocole Aegis (Darksea)  
- **Titre** : Aegis Protocol : Épervier  

---

*Prototype de simulation d’engagement aérien de précision. Aucun lien avec des opérations réelles.*
