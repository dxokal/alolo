# axice pour Codex CLI

Codex CLI a son propre système de "skills" (dossier `SKILL.md` + frontmatter
`name`/`description`), très proche de celui de Claude Code — le portage est
quasi direct, sans commandes séparées : Codex n'a plus de système de
commandes personnalisées (déprécié en faveur des skills), donc chaque étape
(niche, branding, offre...) se déclenche en langage naturel ou via `$axice`.

## Installation

Copie le dossier `axice/` à l'un de ces emplacements, selon la portée
voulue :

**Pour un seul projet** (recommandé) :
```bash
mkdir -p .agents/skills
cp -r integrations/codex/.agents/skills/axice .agents/skills/axice
```

**Pour tous tes projets** :
```bash
mkdir -p "$HOME/.agents/skills"
cp -r integrations/codex/.agents/skills/axice "$HOME/.agents/skills/axice"
```

## Utilisation

- **Implicite** : parle simplement de lancer un business, trouver une
  niche, structurer une offre, etc. — Codex active la skill si la demande
  correspond à sa description.
- **Explicite** : tape `$axice` dans Codex CLI pour forcer son activation.
- Pour une étape précise, demande-la en langage naturel ("fais le branding
  de ce business", "calcule la rentabilité de l'offre") — il n'y a pas
  d'équivalent aux commandes slash `/niche`, `/offre`... de la version
  Claude Code, tout passe par cette skill unique.

Les livrables sont écrits aux mêmes emplacements que dans la version
Claude Code : `business/<slug>/01-niche.md` à `10-onboarding.md`.
