# axice — Plugin de lancement de business (Claude Code)

Plugin Claude Code pour accompagner le lancement d'un business de service
(agence, freelance, conseil, drop-servicing...), de la recherche de niche à
la prospection des premiers clients. La structuration de l'entreprise
(formalités, régime fiscal) part par défaut du contexte Bénin/OHADA, mais
le marché ciblé peut être n'importe quel pays d'Afrique ou du monde
francophone (devise, moyens de paiement et ton adaptés en conséquence).

Chaque étape est consignée dans un fichier markdown persistant (dossier
`business/<slug>/` dans ton répertoire de travail), et la recherche de
niche s'appuie sur des recherches web approfondies plutôt que sur de simples
connaissances générales.

## Contenu du plugin

- **Skill `axice`** : la méthodologie complète (niche, offre, landing page,
  recrutement, prospection), déclenchée automatiquement dès que la
  conversation porte sur le lancement d'un business.
- **Commandes slash** :
  - `/lancer-business [idée / secteur]` — parcours complet, étape par étape.
  - `/niche [secteur ou cible]` — trouver une niche rentable (avec
    recherche web).
  - `/offre [entreprise] [cible] [livrable]` — structurer l'offre et le prix.
  - `/landing-page [entreprise]` — rédiger la page de vente.
  - `/recrutement [profil recherché]` — rédiger une annonce pour trouver un
    prestataire.
  - `/prospection [cible]` — rédiger des messages de cold outreach.
- **Livrables** : chaque commande écrit son résultat dans
  `business/<slug>/0X-etape.md` (voir `skills/axice/SKILL.md` pour le détail
  du nommage), en réutilisant le contexte des fichiers déjà présents.

## Installation

Depuis Claude Code, ajoute ce dépôt comme source de plugin :

```
/plugin marketplace add dxokal/alolo
/plugin install axice
```

(Ou en local si tu as cloné le dépôt : `/plugin marketplace add /chemin/vers/alolo`.)

## Utilisation

Une fois installé, tape par exemple :

```
/lancer-business agence de création de contenu pour marques e-commerce
```

ou lance une étape isolée avec `/niche`, `/offre`, `/landing-page`,
`/recrutement`, `/prospection`.
