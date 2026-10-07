# Prairie Orbitale

Jeu de plateforme 3D pour enfants : un petit robot explore des îles flottantes, ramasse des anneaux, aide les habitants, prépare des gâteaux et s'occupe de son animal.

**Version 7.9**

## Jouer

Ouvre `index.html` dans un navigateur récent. Tout le jeu tient dans ce seul fichier : la bibliothèque 3D (three.js r128) est intégrée, il n'y a donc rien à installer et le jeu se lance même sans connexion (seules les polices Google Fonts demandent Internet, le jeu a des polices de secours).

### Mettre le jeu en ligne avec GitHub Pages

1. Envoie ces fichiers à la racine d'un dépôt GitHub.
2. Dans le dépôt : **Settings → Pages**.
3. Dans **Source**, choisis **Deploy from a branch**, puis la branche `main` et le dossier `/ (root)`.
4. Après une minute, le jeu est accessible à l'adresse `https://<ton-nom>.github.io/<nom-du-dépôt>/`.

## Commandes

| Action | Clavier | Tactile | Manette |
|---|---|---|---|
| Se déplacer | Z Q S D ou flèches | Pouce gauche | Stick gauche / croix |
| Sauter | Espace | Bouton Saut | A |
| Planer | Maintenir Espace en l'air | Maintenir Saut | Maintenir A |
| Tourner la caméra | J / L ou glisser la souris | Glisser à droite | Stick droit (gauche/droite) |
| Incliner la caméra | U / O ou glisser la souris vers le haut/bas | Glisser à droite vers le haut/bas | Stick droit (haut/bas) |
| Recentrer la caméra | K | Double-tap à droite | Clic du stick droit |
| Recentrage automatique | Se fait seul en marchant · réglable dans Pause ou sur l’écran titre (« Caméra auto ») | idem | idem |
| Sac | B ou I | Bouton sac | — |
| Pause | Échap ou P | Bouton pause | Start |

## Sauvegarde

Sur GitHub Pages (ou en ouvrant le fichier directement), la partie est enregistrée dans le navigateur de l'appareil. La sauvegarde en ligne entre appareils ne fonctionne que dans la version publiée comme artefact Claude.

## Nouveautés de la 7.9

- Recentrage automatique de la caméra : quand le robot avance et qu'on ne touche pas à la caméra pendant un instant, elle revient doucement se placer derrière lui et retrouve sa hauteur normale.
- Elle ne fait jamais de demi-tour brusque quand le robot revient vers la caméra, et tourne lentement quand il marche de côté.
- Dès qu'on manipule la caméra (souris, doigt, J/L/U/O, stick droit), le recentrage se met en pause.
- Option « Caméra auto » sur l'écran titre et « Recentrage auto : oui / non » dans le menu Pause (le choix est mémorisé).

## Nouveautés de la 7.8

- La caméra s'incline maintenant aussi de haut en bas : vue d'en haut ou vue rasante, à la souris, au doigt, au clavier (U / O) ou à la manette.
- La hauteur de caméra revient au cadrage normal en recentrant et au début de chaque niveau.

## Crédits

- Jeu : F.S.M Game House
- Moteur 3D : [three.js](https://threejs.org) r128 — © 2010-2021 Three.js Authors, licence MIT (mention conservée dans `index.html`)
- Polices : Lilita One et Nunito (Google Fonts, licence SIL Open Font License)
