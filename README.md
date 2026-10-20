# AEGIS PROTOCOL : VAUTOUR

**v0.3 « LE DÉBARQUEMENT »** — simulation d'opérateur de drone **MALE** : interception de drones ennemis, appui aérien rapproché et conduite d'un réseau d'escouades au sol.

Vous êtes l'**opérateur du drone VAUTOUR 09** au-dessus de la zone charnière **TALIS-V** (région de MERIK), face à l'**AVO**. · F.S.M Game House

> Ce dépôt (*Le-Jardin-Clos*) héberge l'actuel volet de la série Aegis Protocol ; le volet précédent *Épervier 2.8* reste accessible dans l'historique git. Auparavant : *Le Jardin clos*, *Prairie Orbitale*.

## Jouer

Ouvre `index.html` dans un navigateur récent **avec WebGL2** (Chrome, Edge, Firefox, Safari récents).  
Tout le jeu tient dans ce seul fichier : aucun serveur, aucune installation.

**GitHub Pages** — Settings → Pages → *Deploy from a branch* → branche `main` → dossier `/ (root)` :  
`https://wwwh8hv4w5-lang.github.io/Le-Jardin-Clos/`

## Le concept

- **Fréquence nerveuse** : le Vautour 09 évolue en **orbite elliptique à 4 000 m** ; la boule optronique (EOS / IR / mode actif) couvre une zone de **~35 km²** — montagnes au nord, champs au sud, villes et points de contrôle à l'ouest, la route ÉTAT 03 et la route côtière vers l'est.
- **Interception de drones AVO** : chaque drone hostile (kamikaze **ATT**, bombardier **ASM**, reconnaissance **PRD**) franchit jusqu'à **3 lignes de croisement**. Visez le segment d'interception prédit (**MAC**) et tirez au bon moment — marge d'erreur ~2 s, confirmation ~2 s après l'impact. Sans balisage actif ni suivi constant, l'interception est très difficile : les détecteurs ne les voient qu'au moment de l'impact.
- **Alerte MWS** : l'alerte jaune signale les missiles détectés, l'alarme rouge que le drone est frappé.
- **Soutien au sol** : votre détachement **Alpha** tient une position (RAMNAY) et des escouades amies déclenchent la bataille — appui-feu, marquage laser, maintien de la ligne d'arrêt « SILENCE » à la frontière (ligne de retenue « DIGNITÉ », soutien déclaré « toutes les terres »).

## L'escadron FSM

| Véhicule | Rôle |
|----------|------|
| **Alpha** — Humvee | Votre escouade, stationnée à RAMNAY |
| **FSM02** — Humvee | Escorte |
| **FSM03** | Renfort blindé |
| **APC M3** (8 roues) | Blindé de transport, plus tard dans la campagne |

**Alpha** — Silex (Sergent-chef Karim Benali, mitrailleur M134) · Écho (Caporal-chef Thomas Lerat, pilote, HK416F + LG) · Rapace (Capitaine Hélène Marest, chef de détachement, HK416F, MMP) · Dogue (Sergent Victor Ancel, grenadier, HK416F + LG 6 coups).

**FSM02** — Brume (mitrailleur M2 12,7 mm) · Talus (pilote) · Orage (chef de bord, HK416F, AT4) · Cendre (grenadière, HK416F + LG).

**Chaîne de commandement** : ordonnances du général **DESCHAMPS** ; chef d'état-major **colonel WEIT** (QRF) ; support **FUMBLE** — « Toutes les terres ».

## Campagne (missions)

| Code | Titre |
|------|-------|
| M1 | SUPERVISEUR — interception d'un drone de reconnaissance AVO sur un village éloigné |
| M2 | SIGNAL — effondrement du réseau, sauvetage de l'escorte FSM02 |
| M3 | OPENING — réveil du réseau, attaque en embuscade |
| M4 | POINT DE PASSEMENT — col frontalier, infanterie lourde |
| M5 | STRICT ORDER — reconquête de RAMNAY, coup de théâtre |
| M6 | CONTINUITY — défense du centre de commandement de l'unité |
| M7 | TOTAL WAR — bataille de la frontière : infanterie, APC, blindés |
| M8 | END OF ALL — dernière défense du « vestibule de la paix » |

**Batailles spéciales** : E1 ESTUARY (interception de 5 drones AVO : TIMBER, EMBER, SLEDGE, CLEAVER, HAWK-1) · E2 THE BREATH (escarmouche contre hélicoptère ennemi) · E3 ACT OF WAR (frappe aérienne AVO sur le camp FSM) · E4 FORTRESS (assaut blindé AVO sur la base fortifiée).

## Armement embarqué

- **ATM** — missile air-sol (moteurs jettisonnables, guidage laser)
- **AAM ×4** — missile air-air pour l'interception des drones
- Villes de la zone : ROU, MERIK, KORVA (3 routes, frontière nord) — les infiltrations AVO y déclenchent les batailles (drapeau RVO imposé)

## Commandes

| Action | Touche |
|--------|--------|
| Orienter la caméra | Souris |
| Zoom / FOV | Molette (niveaux 1–2–4–8–16) |
| Choisir un point de vue | Clic |
| Choisir le drone de rechange | Clic droit |
| Systèmes clés | `Verr maj` |
| Mode IR | `I` |
| Choisir les cibles | `R` |
| Radar / actu | `T` |
| Engagement | `Y` |
| Tir immédiat (TIR) | `B` |
| MWS actif | `V` |
| Répéter le briefing | `H` |
| Messages | `G` |
| Retour au HQ | `M` |
| Vos ordres | `N` |
| Fusée éclairante | `K` |
| Réveil automatique | `P` |
| Plein écran | `F11` |

## Feuille de route v0.4

- Identification fine des cibles au sol, accompagnement rapproché des soldats au sol
- Compte de munitions et gestion des stocks
- Compagnie K : 1 porte-drone + 2 drones assaillants
- Écran des membres d'équipage, standard de commandement d'infanterie, messages d'urgence
- IA commander : réponses passives, aide au placement, navigation des cibles ennemies, contrôles tactiques
- Événement spécial de fin de campagne : élimination du chef d'état-major AVO — ou nouvel acteur ?

## Technique

- **Runtime « Naval Strike Simulation » v1.2.4** (moteur custom WebGL2)
- Échelle : 1 unité ≈ 10 m ; drone en orbite elliptique à 4 000 m
- Monde généré par mission : terrain, routes, bâtiments, végétation, IA véhicules/personnes
- Vision EOS / IR / mode actif, ombres centrées sur la visée, MWS
- Sauvegarde de campagne navigateur (`APVAUTOUR_SAVE`)

## Fichiers

| Fichier | Rôle |
|---------|------|
| `index.html` | Jeu complet (UI + moteur 3D + missions + IA) |
| `README.md` | Ce document |

## Crédits

- **Jeu** : F.S.M Game House / FERAL SYSTEM MEDIA
- **Moteur 3D** : base *Naval Strike Simulation* (Darksea) / protocole Aegis
- **Titre** : Aegis Protocol : Vautour

---

*Prototype de simulation d'engagement aérien de précision. Aucun lien avec des opérations réelles.*
