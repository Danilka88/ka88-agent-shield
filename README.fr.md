# ka88-agent-shield

Audit de sécurité professionnel pour agents IA.

## Description

ka88-agent-shield est une compétence pour agents IA offrant une protection complète contre :
- Injection de Prompts (Prompt Injection)
- Attaques SSRF
- Exfiltration de Credentials
- JavaScript Malveillant
- Modèles de Phishing
- Obscurcissement (code caché)

## Fonctionnalités

### 🔍 Système d'Audit en 4 Phases

1. **Pre-Visit Scan** — Vérifier l'URL avant la visite
2. **Content Analysis** — Analyser le contenu pour les menaces
3. **Command Safety** — Valider les commandes avant exécution
4. **Self-Audit** — Auto-surveillance périodique

### 📊 216 Modèles de Détection

Ensemble complet de modèles basé sur ClawGuard et OWASP Agentic AI Top 10.

## Installation

### Via OpenSkills (recommandé)

```bash
# Cloner le dépôt
git clone <repo-url> security-auditor-pro
cd security-auditor-pro

# Installation globale
openskills install ./ --global
openskills sync --yes

# Ou installation locale
openskills install ./
openskills sync --yes
```

### Manuel

```bash
# Cloner le dépôt
git clone <repo-url> security-auditor-pro

# Créer un lien symbolique
mkdir -p ~/.claude/skills
ln -s $(pwd)/security-auditor-pro ~/.claude/skills/security-auditor-pro
```

## Utilisation

### Scan Rapide (sans LLM)

```bash
./scripts/quick-scan.sh <chemin> [options]
```

### Scan Complet (avec LM Studio)

```bash
./scripts/scan-skill-scanner.sh <chemin> [options]
```

## Compatibilité

- ✅ OpenCode
- ✅ Claude Code (via OpenSkills)
- ✅ Cursor (via OpenSkills)
- ✅ Windsurf (via OpenSkills)
- ✅ OpenClaw
- ✅ Tout agent avec support SKILL.md

## Licence

MIT

## Version

1.1.0