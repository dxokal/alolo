---
description: Met à jour le pipeline de prospects (ajout, statut, relances) et dit qui relancer.
argument-hint: [slug du business] [action : ajouter un contact / changer un statut / qui relancer]
---

Applique l'étape "Suivi de prospection" de la skill `axice`.

Demande / information donnée par l'utilisateur : $ARGUMENTS

Travaille sur `business/<slug>/07-suivi-prospects.md` :
- S'il n'existe pas, crée-le avec l'en-tête de colonnes défini dans la
  skill (`Contact | Entreprise | Canal | Date contact | Statut |
  Prochaine action | Date relance | Notes`).
- S'il existe, lis-le entièrement avant d'agir — ne jamais répondre "qui
  relancer" ou "où j'en suis" sans l'avoir relu.

Selon la demande :
- **Ajouter un ou plusieurs prospects** : ajoute une ligne par prospect,
  statut initial `à contacter` ou `envoyé` selon ce que l'utilisateur
  indique.
- **Changer un statut** (répondu, converti, perdu...) : met à jour la ligne
  correspondante, et la date de relance si pertinent (3-4 jours ouvrés
  après un envoi sans réponse, jusqu'à 2 relances avant `perdu`).
- **"Qui dois-je relancer"** : liste dans le chat les lignes dont la date
  de relance est arrivée ou dépassée, avec le canal et une suggestion de
  message de relance court.
- **Un prospect passe à `converti`** : signale que les étapes `/contrat` et
  `/onboarding` prennent le relais pour ce client.

Si plusieurs slugs existent sous `business/` et que l'utilisateur n'a pas
précisé lequel, demande lequel avant d'agir.
