---
description: Fait le point sur l'état d'avancement d'un business (ou liste tous les business en cours).
argument-hint: [slug du business - optionnel]
---

Applique la logique de reprise de contexte de la skill `axice`.

Slug donné par l'utilisateur (optionnel) : $ARGUMENTS

**Si aucun slug n'est donné** : liste tous les dossiers présents sous
`business/`. Pour chacun, indique en une ligne quelles étapes ont déjà un
fichier (`01-niche.md` à `10-onboarding.md`) et laquelle manque en premier
dans l'ordre de la méthodologie — c'est la prochaine action recommandée.
S'il n'y a aucun dossier `business/`, dis-le et propose `/lancer-business`
ou `/niche` pour démarrer. Si `11-tunnel.md` existe pour un business,
mentionne-le comme add-on technique déjà en place, mais ne le compte
jamais comme une étape manquante dans la progression 01 → 10 (il est
optionnel et indépendant de l'avancement du reste).

**Si un slug est donné** : lis tous les fichiers présents dans
`business/<slug>/` et produis un résumé dans le chat (pas un nouveau
fichier) :
- Nom du business, niche, positionnement (depuis les fichiers disponibles).
- Étapes complétées vs étapes manquantes, dans l'ordre 01 → 10.
- Si `07-suivi-prospects.md` existe : nombre de prospects par statut, et
  qui est à relancer maintenant.
- Si `11-tunnel.md` existe : signale que le tunnel d'acquisition technique
  a été mis en place (sinon ne le mentionne pas comme une étape en
  attente — c'est un add-on optionnel, pas une étape 01 → 10).
- La prochaine action concrète recommandée (quelle commande lancer).

Ne régénère jamais le contenu des étapes déjà faites — ce n'est qu'un état
des lieux à partir de ce qui existe déjà sur disque.
