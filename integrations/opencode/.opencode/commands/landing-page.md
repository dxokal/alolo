---
description: Rédige le copywriting complet d'une landing page qui convertit.
---

Étape "Landing page" (voir AGENTS.md pour les règles générales).

Contexte donné par l'utilisateur (nom d'entreprise, offre) : $ARGUMENTS

Si `business/<slug>/02-branding.md` et/ou `03-offre.md` existent déjà,
lis-les d'abord pour reprendre le nom et l'offre exacts. Sinon, si l'offre
n'a pas encore été structurée dans la conversation, demande les éléments
clés (promesse, livrables, prix, garantie, cible) avant de rédiger.
Ensuite, rédige le texte complet (pas juste un plan) en suivant la
structure : Hero (titre + sous-titre + CTA + preuve sociale) → Ancien
modèle vs nouveau modèle → Solution/processus en 3-4 étapes → Livrables &
bénéfices → Pricing & garantie (devise adaptée au marché cible, moyens de
paiement locaux si pertinent) → FAQ traitant des objections courantes pour
cette cible.

Consigne le résultat dans `business/<slug>/04-landing-page.md` et indique
le chemin du fichier à l'utilisateur. Suggère ensuite `/recrutement` comme
étape suivante.
