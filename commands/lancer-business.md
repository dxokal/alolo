---
description: Parcours complet pour lancer un business de service, de la niche à l'onboarding client.
argument-hint: [idée, secteur ou marché cible - optionnel]
---

Applique la méthodologie de la skill `axice` pour accompagner l'utilisateur
du début à la fin du lancement de son business.

Idée / secteur / marché de départ donné par l'utilisateur : $ARGUMENTS

Détermine (ou propose) un slug pour ce business dès le départ et crée le
dossier `business/<slug>/` : tous les livrables seront écrits au fur et à
mesure, pas seulement affichés dans le chat. Si `business/<slug>/` existe
déjà avec des fichiers, reprends à partir de la première étape manquante
au lieu de tout refaire.

Déroule les étapes dans l'ordre, en confirmant chaque étape avec
l'utilisateur avant de passer à la suivante (ne fabrique pas tout d'un coup
sans validation) :

1. **Niche & Hungry Crowd** — si $ARGUMENTS est vide ou trop vague, pose les
   questions nécessaires (secteur, type de client, budget probable, zone
   géographique) ; fais des recherches web approfondies (marché,
   concurrents, prix, signaux de demande) avant de proposer des pistes de
   niche avec recommandation. Écris `business/<slug>/01-niche.md`.
2. **Branding** — nom, baseline, ton de marque, éléments visuels de base.
   Écris `business/<slug>/02-branding.md`.
3. **Offre irrésistible** — promesse, livrables, pricing (devise adaptée
   au marché cible) et garantie, comme hypothèse à revalider à l'étape 6.
   Écris `business/<slug>/03-offre.md`.
4. **Landing page** — copywriting complet une fois l'offre validée. Écris
   `business/<slug>/04-landing-page.md`.
5. **Recrutement** — annonce pour trouver les prestataires, avec
   estimation de coût par livrable/mois. Écris
   `business/<slug>/05-recrutement.md`.
6. **Finances** — marge par client, seuil de rentabilité, prévisionnel
   3-6 mois à partir du prix (étape 3) et du coût prestataire (étape 5).
   Si ça ne tient pas, le dire et ajuster avant de continuer. Écris
   `business/<slug>/08-finances.md`.
7. **Prospection** — messages de cold outreach adaptés à la cible (B2B
   institutionnel vs PME vs particuliers). Écris
   `business/<slug>/06-prospection.md`, puis initialise le pipeline
   `business/<slug>/07-suivi-prospects.md`.

Pour le reste (contrat/CGV et onboarding), n'anticipe pas automatiquement :
propose-les quand l'utilisateur signale un prospect converti, en renvoyant
vers `/contrat` puis `/onboarding`.

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
dans `business/<slug>/` et rappelle que `/business-status <slug>` permet de
reprendre le point à tout moment.
