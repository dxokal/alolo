# alolo — Plugin de lancement de business (Claude Code)

Plugin Claude Code pour accompagner le lancement d'un business de service
(agence, freelance, conseil, drop-servicing...), de la recherche de niche à
la prospection des premiers clients. Méthodologie adaptée au contexte
Bénin / OHADA / UEMOA (FCFA, formalités, paiement mobile money).

## Contenu du plugin

- **Skill `lancement-business`** : la méthodologie complète (niche, offre,
  landing page, recrutement, prospection), déclenchée automatiquement dès
  que la conversation porte sur le lancement d'un business.
- **Commandes slash** :
  - `/lancer-business [idée / secteur]` — parcours complet, étape par étape.
  - `/niche [secteur ou cible]` — trouver une niche rentable.
  - `/offre [entreprise] [cible] [livrable]` — structurer l'offre et le prix.
  - `/landing-page [entreprise]` — rédiger la page de vente.
  - `/recrutement [profil recherché]` — rédiger une annonce pour trouver un
    prestataire.
  - `/prospection [cible]` — rédiger des messages de cold outreach.

## Installation

Depuis Claude Code, ajoute ce dépôt comme source de plugin :

```
/plugin marketplace add dxokal/alolo
/plugin install lancement-business
```

(Ou en local si tu as cloné le dépôt : `/plugin marketplace add /chemin/vers/alolo`.)

## Utilisation

Une fois installé, tape par exemple :

```
/lancer-business agence de création de contenu pour marques e-commerce
```

ou lance une étape isolée avec `/niche`, `/offre`, `/landing-page`,
`/recrutement`, `/prospection`.
