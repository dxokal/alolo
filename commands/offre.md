---
description: Structure une offre irrésistible (promesse, livrables, prix, garantie).
argument-hint: [nom de l'entreprise] [cible] [livrable principal]
---

Applique l'étape "Offre irrésistible" de la skill `axice`.

Éléments donnés par l'utilisateur (nom d'entreprise, cible, livrable) :
$ARGUMENTS

Si `business/<slug>/01-niche.md` et/ou `02-branding.md` existent déjà,
lis-les d'abord pour garder la cohérence (niche retenue, nom choisi). Si
des éléments manquent, demande-les. Sinon, produis :
1. Une promesse unique (USP) en une phrase percutante.
2. La décomposition des livrables en bénéfices clairs pour le client.
3. Un positionnement tarifaire dans la devise adaptée au marché cible, avec
   au moins deux paliers (offre d'entrée / offre scale), cohérent avec le
   type de cible (PME vs grand compte/institution).
4. Une structure de garantie réaliste et soutenable pour l'utilisateur.

Signale que ce prix est une hypothèse à revalider financièrement une fois
les coûts de prestataires connus (`/finances`, étape 8).

Consigne le résultat dans `business/<slug>/03-offre.md` et indique le
chemin du fichier à l'utilisateur. Suggère ensuite `/landing-page` comme
étape suivante.
