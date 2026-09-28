---
description: Parcours complet pour lancer un business de service, de la niche à la prospection.
argument-hint: [idée, secteur ou marché cible - optionnel]
---

Applique la méthodologie de la skill `axice` pour accompagner l'utilisateur
du début à la fin du lancement de son business.

Idée / secteur / marché de départ donné par l'utilisateur : $ARGUMENTS

Détermine (ou propose) un slug pour ce business dès le départ et crée le
dossier `business/<slug>/` : tous les livrables des 5 étapes y seront
écrits au fur et à mesure, pas seulement affichés dans le chat.

Déroule les 5 étapes dans l'ordre, en confirmant chaque étape avec
l'utilisateur avant de passer à la suivante (ne fabrique pas tout d'un coup
sans validation) :

1. **Niche & Hungry Crowd** — si $ARGUMENTS est vide ou trop vague, pose les
   questions nécessaires (secteur, type de client, budget probable, zone
   géographique) ; fais des recherches web approfondies (marché,
   concurrents, prix, signaux de demande) avant de proposer des pistes de
   niche avec recommandation. Écris `business/<slug>/01-niche.md`.
2. **Offre irrésistible** — une fois la niche validée, structure la
   promesse, les livrables, le pricing (devise adaptée au marché cible) et
   la garantie. Écris `business/<slug>/02-offre.md`.
3. **Landing page** — rédige le copywriting complet une fois l'offre
   validée. Écris `business/<slug>/03-landing-page.md`.
4. **Recrutement** — rédige l'annonce pour trouver les prestataires qui
   livreront le service. Écris `business/<slug>/04-recrutement.md`.
5. **Prospection** — rédige les messages de cold outreach pour les premiers
   clients, adaptés à la cible (B2B institutionnel vs PME vs particuliers).
   Écris `business/<slug>/05-prospection.md`.

Termine par le tableau "Plan d'exécution synthétique" rempli et adapté au
contexte de ce business précis (délais réalistes, canaux choisis), écrit
dans `business/<slug>/00-plan-execution.md`.

Rappelle-toi des règles de sortie de la skill : français, ton pro et
chaleureux pour les documents commerciaux, devise adaptée à la zone
géographique ciblée par le client (pas de FCFA par défaut si la cible n'est
pas en zone UEMOA/CEMAC), options avec coûts/risques/recommandation pour
toute décision structurante, et signale les points juridiques/fiscaux
pertinents (structuration de l'entreprise de l'utilisateur au Bénin/OHADA
par défaut, réglementation locale côté client si différente) sans en faire
un cours. À la fin, récapitule dans le chat la liste des fichiers créés
dans `business/<slug>/`.
