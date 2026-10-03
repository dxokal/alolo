---
description: Trouve un nom, une baseline et un positionnement de marque pour le business.
argument-hint: [niche ou idée de nom - optionnel]
---

Applique l'étape "Branding" de la skill `axice`.

Contexte donné par l'utilisateur : $ARGUMENTS

Si `business/<slug>/01-niche.md` existe déjà, lis-le d'abord pour ancrer le
branding dans la niche retenue (cible, zone géographique, positionnement).
Sinon, demande au moins le secteur/la niche avant de proposer des noms.

Propose 5 à 8 pistes de nom (courtes, prononçables, vérifiées par recherche
web pour éviter un conflit évident dans la même niche/zone), une baseline,
un ton de marque (3-4 adjectifs), et des éléments visuels de base
(palette/style à briefer à un designer). Recommande un nom avec sa raison.

Consigne le résultat dans `business/<slug>/02-branding.md` et indique le
chemin du fichier à l'utilisateur. Si le slug du dossier business était
provisoire (basé sur la niche), propose de le renommer selon le nom choisi.
Suggère ensuite `/offre` comme étape suivante.
