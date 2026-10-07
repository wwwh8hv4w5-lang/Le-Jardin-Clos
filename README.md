# Prairie Orbitale

Jeu de plateforme 3D pour enfants : un petit robot explore des îles flottantes, ramasse des anneaux, aide les habitants, prépare des gâteaux et s'occupe de son animal.

**Version 8.2**

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
| S’envoler | Marcher dans un tourbillon ou sur un nuage rose, puis se diriger | idem | idem |
| S’asseoir / entrer | Bouton d’action près d’un banc ou d’une porte | idem | idem |
| Recentrage automatique | Se fait seul en marchant · réglable dans Pause ou sur l’écran titre (« Caméra auto ») | idem | idem |
| Sac | B ou I | Bouton sac | — |
| Pause | Échap ou P | Bouton pause | Start |

## Sauvegarde

Sur GitHub Pages (ou en ouvrant le fichier directement), la partie est enregistrée dans le navigateur de l'appareil. La sauvegarde en ligne entre appareils ne fonctionne que dans la version publiée comme artefact Claude.

## Nouveautés de la 8.2 — iPhone et iPad

- Le jeu a été vérifié sur des écrans d'iPhone (13, SE, en portrait et en paysage) et d'iPad (en portrait).
- L'entrée et la sortie de l'Observatoire ne figent plus le jeu : la pièce n'ajoute plus de lampe, qui obligeait Safari à recalculer tout l'éclairage.
- Sur les petits écrans (iPhone SE), le nom de l'île ne chevauche plus le compteur d'anneaux, et l'astuce de caméra ne gêne plus le joystick.
- L'astuce de caméra devient « Glisser pour regarder ».

## Nouveautés de la 8.1

**L'Observatoire des Nuages se visite**
- À l'intérieur, on trouve le Professeur Lunette, la grande lunette, un planétaire qui tourne, un globe et des affiches du ciel.
- Pour 8 anneaux, le professeur vend un billet qui donne droit à 30 secondes dans le télescope.
- Dans le télescope, on fait glisser le doigt pour regarder les étoiles, les étoiles filantes, Saturne, Jupiter, Mars, la Lune et Neptune.
- Un petit robot passe en vaisseau spatial et fait coucou.

**Les bancs**
- Les bancs sont solides : on ne passe plus au travers.
- On peut s'asseoir dessus avec le bouton « S'asseoir ». Pour se relever, on bouge, on saute, ou on appuie sur « Se lever ».

**Corrections**
- Le décor ne devient plus transparent : la caméra se tourne et s'incline librement.
- Les îles de décor lointaines n'apparaissent plus au milieu du parcours, par exemple au-dessus du phare.

## Nouveautés de la 8.0 — la grande mise à jour des Îles Flottantes

**Un archipel à explorer**
- Les îles ont des formes arrondies, avec des avancées, et plusieurs îlots flottent dans le ciel.
- Le chemin principal reste entièrement faisable à pied grâce aux ponts à barrières.
- Les chemins secondaires passent par le ciel : tourbillons de vent, nuages rebondissants, passerelle suspendue et plateforme-navette.

**De nouveaux lieux**
- L'Observatoire des Nuages, avec sa coupole qui tourne, sa grande lunette, son trésor et Stella l'astronome.
- Une cascade qui tombe dans le vide, sous un arc-en-ciel.
- Le petit phare des nuages, avec sa lumière qui tourne.
- L'îlot du petit robot perdu, dans le ciel, et un îlot-trésor dans les nuages.

**Trois nouvelles quêtes**
- Gaston et son carillon à vent.
- Rosa et le premier vol de ses oisillons.
- Félix et sa montgolfière miniature.

**Une nouvelle mécanique : le vent**
- On marche dans un tourbillon qui brille : il emporte le robot tout là-haut.
- Les nuages roses font rebondir le robot.
- Ensuite, le vent le porte : il plane tout seul, il n'y a qu'à se diriger.
- Quand on vole, on peut passer au-dessus des barrières et atterrir sur une île depuis l'extérieur.
- Les barrières empêchent toujours de tomber en marchant.
- Pip explique tout la première fois.

## Nouveautés de la 7.10

- Console propre : suppression des avertissements « flatShading » de three.js qui s’affichaient en boucle (aucun changement visuel).

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
