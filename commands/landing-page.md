---
description: Rédige le copywriting complet d'une landing page qui convertit.
argument-hint: [nom de l'entreprise et rappel rapide de l'offre]
---

Applique l'étape "Landing page" de la skill `axice`.

Contexte donné par l'utilisateur (nom d'entreprise, offre) : $ARGUMENTS

Si `business/<slug>/02-offre.md` existe déjà, lis-le d'abord pour reprendre
l'offre exacte. Sinon, si l'offre n'a pas encore été structurée dans la
conversation, demande les éléments clés (promesse, livrables, prix,
garantie, cible) avant de rédiger. Ensuite, rédige le texte complet (pas
juste un plan) en suivant la structure : Hero (titre + sous-titre + CTA +
preuve sociale) → Ancien modèle vs nouveau modèle → Solution/processus en
3-4 étapes → Livrables & bénéfices → Pricing & garantie (devise adaptée au
marché cible, moyens de paiement locaux si pertinent) → FAQ traitant des
objections courantes pour cette cible.

Consigne le résultat dans `business/<slug>/03-landing-page.md` et indique
le chemin du fichier à l'utilisateur.
