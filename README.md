# axice — Plugin de lancement de business (Claude Code)

Plugin Claude Code pour accompagner le lancement d'un business de service
(agence, freelance, conseil, drop-servicing...), de la recherche de niche à
l'onboarding du premier client. La structuration de l'entreprise
(formalités, régime fiscal) part par défaut du contexte Bénin/OHADA, mais
le marché ciblé peut être n'importe quel pays d'Afrique ou du monde
francophone (devise, moyens de paiement et ton adaptés en conséquence).

Chaque étape est consignée dans un fichier markdown persistant (dossier
`business/<slug>/` dans ton répertoire de travail), la recherche de niche
s'appuie sur des recherches web approfondies, et un pipeline de prospection
garde la trace des relances.

## Contenu du plugin

- **Skill `axice`** : la méthodologie complète en 10 étapes, déclenchée
  automatiquement dès que la conversation porte sur le lancement d'un
  business.
- **Commandes slash** :
  - `/lancer-business [idée / secteur]` — parcours complet, étape par étape.
  - `/niche [secteur ou cible]` — trouver une niche rentable (avec
    recherche web).
  - `/branding [niche ou idée de nom]` — nom, baseline, ton de marque.
  - `/offre [entreprise] [cible] [livrable]` — structurer l'offre et le prix.
  - `/landing-page [entreprise]` — rédiger la page de vente.
  - `/recrutement [profil recherché]` — rédiger une annonce pour trouver un
    prestataire.
  - `/prospection [cible]` — rédiger des messages de cold outreach.
  - `/pipeline [slug] [action]` — ajouter/mettre à jour des prospects,
    savoir qui relancer.
  - `/finances [slug]` — marge par client, seuil de rentabilité,
    prévisionnel.
  - `/contrat [slug ou client]` — CGV + trame de contrat client.
  - `/onboarding [client ou slug]` — kickoff et suivi du nouveau client.
  - `/tunnel [slug - optionnel]` — transformer une landing page existante
    en tunnel d'acquisition technique (capture, notification, relances,
    suivi de statut) — add-on optionnel qui produit aussi du code
    applicatif, à lancer une fois `/landing-page` fait.
  - `/business-status [slug]` — état d'avancement d'un business, ou liste
    de tous les business en cours si aucun slug n'est donné.

## Structure des livrables

Chaque commande écrit son résultat dans `business/<slug>/`, en réutilisant
le contexte des fichiers déjà présents :

```
business/<slug>/
  00-plan-execution.md
  01-niche.md
  02-branding.md
  03-offre.md
  04-landing-page.md
  05-recrutement.md
  06-prospection.md
  07-suivi-prospects.md   # pipeline, mis à jour en continu
  08-finances.md
  09-contrat-cgv.md
  10-onboarding.md
  11-tunnel.md            # optionnel, add-on technique (voir /tunnel)
```

Voir `skills/axice/SKILL.md` pour le détail de chaque étape.

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

ou lance une étape isolée avec `/niche`, `/branding`, `/offre`,
`/landing-page`, `/recrutement`, `/prospection`, `/pipeline`, `/finances`,
`/contrat`, `/onboarding`, ou encore `/tunnel` une fois la landing page
prête pour la transformer en tunnel d'acquisition technique (capture,
notification, relances, suivi de statut). Utilise `/business-status` à
tout moment pour savoir où tu en es.

## Codex CLI et OpenCode

Le format de plugin ci-dessus (`.claude-plugin/`, commandes slash,
`SKILL.md` à déclenchement auto) est spécifique à Claude Code. Le dossier
[`integrations/`](integrations/) contient une adaptation du même contenu
pour ces deux autres outils, avec leurs propres mécanismes d'extension.

### Codex CLI

Skill Codex (`.agents/skills/axice/SKILL.md`), portage quasi direct :

```bash
# pour un seul projet
mkdir -p .agents/skills
cp -r integrations/codex/.agents/skills/axice .agents/skills/axice

# ou pour tous tes projets
mkdir -p "$HOME/.agents/skills"
cp -r integrations/codex/.agents/skills/axice "$HOME/.agents/skills/axice"
```

Puis parle simplement de lancer un business, ou tape `$axice` pour forcer
son activation. Détails : [`integrations/codex/README.md`](integrations/codex/README.md).

### OpenCode

`AGENTS.md` (règles toujours chargées) + commandes `.opencode/commands/*.md` :

```bash
# pour un seul projet
cp integrations/opencode/AGENTS.md ./AGENTS.md
mkdir -p .opencode/commands
cp integrations/opencode/.opencode/commands/*.md .opencode/commands/

# ou pour tous tes projets
cp integrations/opencode/AGENTS.md "$HOME/.config/opencode/AGENTS.md"
mkdir -p "$HOME/.config/opencode/commands"
cp integrations/opencode/.opencode/commands/*.md "$HOME/.config/opencode/commands/"
```

Si le projet a déjà un `AGENTS.md`, fusionne le contenu à la main plutôt
que de l'écraser. Mêmes commandes slash qu'avec Claude Code (`/niche`,
`/offre`, etc.). Détails : [`integrations/opencode/README.md`](integrations/opencode/README.md).
