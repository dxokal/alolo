---
description: Structure l'accueil d'un nouveau client signé (kickoff, suivi, renouvellement).
argument-hint: [nom du client ou slug du business - optionnel]
---

Applique l'étape "Onboarding client" de la skill `axice`.

Contexte donné par l'utilisateur : $ARGUMENTS

Lis `business/<slug>/03-offre.md` et `09-contrat-cgv.md` s'ils existent,
pour cadrer l'onboarding sur ce qui a été vendu.

Produis :
1. **Séquence de kickoff** : informations à collecter auprès du client,
   premier échange de cadrage, délai avant la première livraison.
2. **Points de contact récurrents** : fréquence des points d'avancement et
   canal privilégié (email, WhatsApp Business, appel).
3. **Fin de mission/renouvellement** : bilan de fin de mission, demande de
   témoignage/référence, proposition de renouvellement ou de palier
   supérieur.

Consigne le résultat dans `business/<slug>/10-onboarding.md` et indique le
chemin du fichier à l'utilisateur. Si ce client vient du pipeline
(`07-suivi-prospects.md`), rappelle de le marquer `converti` s'il ne l'est
pas déjà.
