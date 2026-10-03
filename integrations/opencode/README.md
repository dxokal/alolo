# axice pour OpenCode

OpenCode n'a pas de système de "skills" à déclenchement automatique : le
contexte permanent passe par `AGENTS.md`, et les étapes individuelles par
des commandes markdown dans `.opencode/commands/` (même syntaxe `$ARGUMENTS`
que les commandes Claude Code — portage quasi direct).

## Installation

**Pour un seul projet** (recommandé) :
```bash
cp integrations/opencode/AGENTS.md ./AGENTS.md
mkdir -p .opencode/commands
cp integrations/opencode/.opencode/commands/*.md .opencode/commands/
```
Si le projet a déjà un `AGENTS.md`, fusionne son contenu à la main plutôt
que de l'écraser (OpenCode ne charge qu'un seul fichier par niveau).

**Pour tous tes projets** :
```bash
cp integrations/opencode/AGENTS.md "$HOME/.config/opencode/AGENTS.md"
mkdir -p "$HOME/.config/opencode/commands"
cp integrations/opencode/.opencode/commands/*.md "$HOME/.config/opencode/commands/"
```

## Utilisation

Les mêmes commandes qu'avec Claude Code : `/lancer-business`, `/niche`,
`/branding`, `/offre`, `/landing-page`, `/recrutement`, `/prospection`,
`/pipeline`, `/finances`, `/contrat`, `/onboarding`, `/tunnel`,
`/business-status`.

`AGENTS.md` étant toujours chargé, tu peux aussi simplement discuter en
langage naturel ("aide-moi à trouver une niche pour mon agence") : OpenCode
aura déjà les règles de sortie, la structure de fichiers et le contexte
juridique/fiscal en tête, même sans taper de commande.

Les livrables sont écrits aux mêmes emplacements que dans la version
Claude Code : `business/<slug>/01-niche.md` à `10-onboarding.md` (plus
`11-tunnel.md` pour l'add-on optionnel `/tunnel`).
