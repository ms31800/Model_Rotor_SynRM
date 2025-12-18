# SynRM & FOC – Visualisations pédagogiques interactives

Ce dépôt propose un **ensemble d’animations interactives** dédiées à la compréhension des **machines synchrones à réluctance (SynRM)** et de leur **commande vectorielle (FOC – Field Oriented Control)**.

### Animation du rotor SynRM – axes d/q, flux et couple
- Animation interactive montrant :
- la géométrie réelle du rotor SynRM (barrières de flux),
- la détection automatique des axes d / q à partir du SVG du rotor,
- le champ magnétique tournant du stator, 
- le flux magnétique anisotrope (évitement des barrières),
- le couple de réluctance instantané :


 Points pédagogiques clés :
- l’axe **d** correspond à la **perméabilité maximale**,
- l’axe **q** est orthogonal et correspond à la **réluctance maximale**,
- le décalage angulaire (≈ 45° ici) dépend **de la géométrie réelle du rotor**.

###  Animation FOC – commande vectorielle
Animation complémentaire: https://ms31800.github.io/FOC-SynRM-Explorer/

 Cette animation fait le lien entre :
- la physique du moteur,  
- la géométrie rotorique,  
- la commande numérique (FOC).

##  Objectifs pédagogiques

Comprendre **le couple de réluctance** sans aimants ni courant rotor
Visualiser la notion d’**anisotropie magnétique**
  Relier :
   - géométrie du rotor,
   - axes d/q,
   - champ statorique,
   - loi de couple
   
##  Technologies utilisées

    **HTML / JavaScript**
    **p5.js**
    **SVG** (géométrie du rotor) importé dans le html pour alléger le code
    Calculs vectoriels temps réel
    Aucune dépendance serveur

## Le gain d'alignement et l'action sur Ld/Lq ne sont visibles qu'en mode non synchrone
le rotor est piloté uniquement par la loi d’alignement et le gain joue pleinement son rôle

On observe :
- le retard angulaire,
- l’oscillation éventuelle,
- la convergence progressive

## Gain d’alignement :
Il règle la “force” avec laquelle le rotor rattrape le champ statorique dans l’animation.
C'est un paramètre numérique contrôlant la vitesse de convergence du rotor vers l’axe d du champ statorique.
Il représente de manière qualitative l’effet combiné du couple de réluctance et de l’inertie mécanique, sans modélisation dynamique complète.
Effet concret du curseur
- Gain faible:  
  - Le rotor met du temps à s’aligner 
  - δ reste plus grand 
  - Animation douce, lente 
  - Analogie : rotor lourd / faible couple
  
- Gain élevé:
  - Le rotor “colle” rapidement au champ
  - δ devient très petit
  - Réponse rapide
  - Peut devenir un peu “nerveux” si trop élevé
  - Analogie : rotor léger / couple élevé
 
 ## Anisotropie magnétique
Ld et Lq sont les inductances vues par le champ statorique selon deux axes orthogonaux du rotor.
Dans un moteur à réluctance synchrone :
- Ld > Lq à cause des barrières de flux
- le rotor s’aligne naturellement pour minimiser la réluctance
C’est ce phénomène, appelé anisotropie magnétique, qui permet la production de couple.
- Le couple produit augmente avec l'anisotropie: T∝(Ld​−Lq​)sin(2δ)

### En ligne (recommandé)
Le projet est hébergé via **GitHub Pages** :
**https://ms31800.github.io/Model_Rotor_SynRM/**

