---
description: Fait le point sur l'état d'avancement d'un business (ou liste tous les business en cours).
---

Logique de reprise de contexte (voir AGENTS.md pour les règles générales).

Slug donné par l'utilisateur (optionnel) : $ARGUMENTS

**Si aucun slug n'est donné** : liste tous les dossiers présents sous
`business/`. Pour chacun, indique en une ligne quelles étapes ont déjà un
fichier (`01-niche.md` à `10-onboarding.md`) et laquelle manque en premier
dans l'ordre de la méthodologie — c'est la prochaine action recommandée.
S'il n'y a aucun dossier `business/`, dis-le et propose `/lancer-business`
ou `/niche` pour démarrer.

**Si un slug est donné** : lis tous les fichiers présents dans
`business/<slug>/` et produis un résumé dans le chat (pas un nouveau
fichier) :
- Nom du business, niche, positionnement (depuis les fichiers disponibles).
- Étapes complétées vs étapes manquantes, dans l'ordre 01 → 10.
- Si `07-suivi-prospects.md` existe : nombre de prospects par statut, et
  qui est à relancer maintenant.
- La prochaine action concrète recommandée (quelle commande lancer).

Ne régénère jamais le contenu des étapes déjà faites — ce n'est qu'un état
des lieux à partir de ce qui existe déjà sur disque.
