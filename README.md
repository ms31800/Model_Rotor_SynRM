# SynRM & FOC – Visualisations pédagogiques interactives

Ce dépôt propose un **ensemble d’animations interactives** dédiées à la compréhension des **machines synchrones à réluctance (SynRM)** et de leur **commande vectorielle (FOC – Field Oriented Control)**.

L’objectif est de fournir un **support visuel rigoureux**, utilisable aussi bien en **enseignement**, en **auto-formation**, qu’en **ingénierie de conception / commande**.


## ✨ Contenu du dépôt

### Animation du rotor SynRM – axes d/q, flux et couple
Animation interactive montrant :

- la **géométrie réelle du rotor SynRM** (barrières de flux),
- la **détection automatique des axes d / q** à partir du SVG du rotor,
- le **champ magnétique tournant** du stator,
- le **flux magnétique anisotrope** (évitement des barrières),
- le **couple de réluctance instantané** :
  \[
  T \propto (L_d - L_q)\sin(2\delta)
  \]

 Points pédagogiques clés :
- l’axe **d** correspond à la **perméabilité maximale**,
- l’axe **q** est orthogonal et correspond à la **réluctance maximale**,
- le décalage angulaire (≈ 45° ici) dépend **de la géométrie réelle du rotor**.


###  Animation FOC – commande vectorielle
Animation complémentaire illustrant :

- les courants triphasés,
- la transformation **Clarke / Park**,
- les axes **d / q tournants**,
- la régulation indépendante :
  - flux (axe d),
  - couple (axe q),
- la synchronisation champ / rotor.

 Cette animation fait le lien entre :
- **la physique du moteur**,  
- **la géométrie rotorique**,  
- **la commande numérique (FOC)**.


##  Objectifs pédagogiques

- Comprendre **le couple de réluctance** sans aimants ni courant rotor
- Visualiser la notion d’**anisotropie magnétique**
- Relier :
  - géométrie du rotor,
  - axes d/q,
  - champ statorique,
  - loi de couple
- Démystifier la **commande FOC** appliquée aux SynRM


##  Technologies utilisées

- **HTML / JavaScript**
- **p5.js**
- **SVG** (géométrie du rotor)
- Calculs vectoriels temps réel
- Aucune dépendance serveur


##  Utilisation

### En ligne (recommandé)
Le projet est hébergé via **GitHub Pages** :

👉 https://<ton-utilisateur>.github.io/<nom-du-depot>/

### En local
```bash
git clone https://github.com/<ton-utilisateur>/<nom-du-depot>.git
cd <nom-du-depot>
