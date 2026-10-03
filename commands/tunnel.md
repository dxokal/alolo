---
description: Transforme une landing page existante en tunnel d'acquisition technique (capture, notification, relances, suivi de statut).
argument-hint: [slug du business - optionnel]
---

Applique l'étape "Tunnel d'acquisition technique" de la skill `axice`.

Contexte donné par l'utilisateur : $ARGUMENTS

Vérifie que `business/<slug>/04-landing-page.md` existe : c'est le texte de
vente que ce tunnel doit mettre en ligne et connecter. S'il n'existe pas,
dis-le et propose de lancer `/landing-page` d'abord. Lis aussi
`02-branding.md` et `03-offre.md` s'ils existent pour le nom, le ton et les
prix à reprendre.

Avant d'écrire du code, produis un plan court et attends l'accord de
l'utilisateur avant de commencer à coder quoi que ce soit :
- **Stack** : Next.js (App Router) + TypeScript strict + Server
  Components, géré avec bun par défaut (ou la stack déjà en place dans ce
  projet si le dépôt courant utilise autre chose).
- **Stockage des prospects** : une option par défaut + au moins 2
  alternatives plus simples, avec leur coût.
- **Notification immédiate** (WhatsApp via lien `wa.me` pré-rempli, ou une
  plateforme WhatsApp Business déjà connectée au compte si disponible,
  et/ou email) : option par défaut + alternatives, avec coût.
- **Hébergement** : option par défaut + au moins 2 alternatives, avec coût.
- Signale clairement tout choix engageant un service payant ou un compte
  externe.

Une fois le plan validé, livre en 3 étapes séparées, chacune validée avant
de passer à la suivante :
1. Landing (mobile-first, légère) + formulaire de capture validé par Zod +
   anti-spam (honeypot + rate limiting) + stockage + notification
   immédiate.
2. Séquence de relances automatiques (avec consentement explicite et lien
   de désinscription).
3. Tableau/vue de suivi des statuts (`nouveau` → `contacté` → `atelier de
   cadrage planifié` → `devis envoyé` → `signé` → `perdu`).

Respecte systématiquement : secrets en variables d'environnement avec
`.env.example` à jour, mentions légales/politique de confidentialité sur la
page, mesure légère uniquement (visite, clic CTA, formulaire envoyé), pas
de paiement en ligne/espace client/CRM complet sauf demande explicite.
Écris au moins un test par fonctionnalité livrée ; ne déclare une étape
terminée qu'une fois lint et tests passants.

Consigne le plan et les décisions prises dans `business/<slug>/11-tunnel.md`
et indique à l'utilisateur à la fois ce chemin et l'emplacement du code
ajouté dans le projet. Rappelle que cette étape reste optionnelle et n'est
pas incluse dans l'enchaînement automatique de `/lancer-business`.
