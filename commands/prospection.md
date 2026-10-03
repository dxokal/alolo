---
description: Rédige des messages de prospection à froid personnalisés pour décrocher les premiers clients.
argument-hint: [cible / persona]
---

Applique l'étape "Acquisition client / prospection" de la skill `axice`.

Cible donnée par l'utilisateur : $ARGUMENTS

Rédige un ou plusieurs modèles de message de prospection à froid suivant :
compliment spécifique et sincère → point faible repéré avec tact → offre de
valeur initiale gratuite et ciblée → question ouverte simple sans pression
commerciale. Adapte le ton et le canal à la cible : plus direct et court
(moins de 100 mots) pour une PME/e-commerçant, plus formel (LinkedIn/email
professionnel, orienté crédibilité et références) pour une institution ou un
grand compte.

Consigne les modèles dans `business/<slug>/06-prospection.md` et indique le
chemin du fichier à l'utilisateur. Si l'utilisateur mentionne des prospects
réellement contactés (ou cite une liste de cibles à contacter), ajoute-les
aussi au pipeline `business/<slug>/07-suivi-prospects.md` (crée-le avec
l'en-tête de colonnes de la skill s'il n'existe pas encore) plutôt que de
les laisser uniquement dans ce fichier de modèles. Suggère ensuite
`/pipeline` pour gérer les relances au fil du temps.
