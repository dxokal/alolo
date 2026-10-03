---
description: Calcule la rentabilité de l'offre (marge par client, seuil de rentabilité, prévisionnel).
---

Étape "Finances" (voir AGENTS.md pour les règles générales).

Contexte donné par l'utilisateur : $ARGUMENTS

Lis `business/<slug>/03-offre.md` (prix) et `business/<slug>/05-recrutement.md`
(coût prestataires) s'ils existent. S'ils manquent, demande au moins le
prix de vente envisagé et une estimation du coût variable par client avant
de calculer quoi que ce soit — ne fabrique pas de chiffres sans base.

Produis :
1. Coûts variables par client/mission (prestataires, outils dédiés, frais
   de paiement, commissions éventuelles).
2. Coûts fixes mensuels de l'activité.
3. Marge par client pour chaque palier de prix.
4. Seuil de rentabilité (nombre de clients/mois pour couvrir les coûts
   fixes).
5. Si la marge ou le seuil ne tiennent pas face au marché identifié à
   l'étape niche, dis-le explicitement et propose des options (prix,
   coût prestataire, périmètre du livrable) avec leurs compromis — ne
   valide jamais une offre non rentable pour rassurer l'utilisateur.
6. Un mini compte de résultat prévisionnel sur 3 à 6 mois (hypothèse
   basse/réaliste/haute de nombre de clients).

Consigne le résultat dans `business/<slug>/08-finances.md`, dans la devise
du marché cible, et indique le chemin du fichier à l'utilisateur.
