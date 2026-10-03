---
description: Rédige des CGV et une trame de contrat client à partir de l'offre validée.
argument-hint: [slug du business ou nom du client - optionnel]
---

Applique l'étape "Contrat / CGV" de la skill `axice`.

Contexte donné par l'utilisateur : $ARGUMENTS

Lis `business/<slug>/03-offre.md` (promesse, livrables, prix, garantie)
s'il existe, pour que le contrat reprenne exactement l'offre vendue. S'il
manque, demande ces éléments avant de rédiger.

Produis :
1. **CGV** : objet, délais de livraison, modalités de paiement (acompte
   usuel 30-50 % à la commande, solde à la livraison), propriété/droits
   d'usage du livrable, confidentialité, limitation de responsabilité,
   conditions de résiliation/remboursement cohérentes avec la garantie de
   l'offre.
2. **Trame de contrat client** courte (1-2 pages) reprenant l'offre
   acceptée et renvoyant aux CGV pour le reste.

Rappelle explicitement que ce sont des modèles de départ à faire relire par
un juriste/expert-comptable local avant signature, surtout les clauses de
responsabilité et de propriété intellectuelle, et à adapter si le client
est une institution avec ses propres procédures contractuelles.

Consigne le résultat dans `business/<slug>/09-contrat-cgv.md` et indique le
chemin du fichier à l'utilisateur. Suggère ensuite `/onboarding` une fois
le contrat signé.
