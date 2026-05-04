# Security Auditor Pro

Professionelles Sicherheitsaudit für KI-Agenten.

## Beschreibung

Security Auditor Pro ist eine Fähigkeit für KI-Agenten, die umfassenden Schutz bietet gegen:
- Prompt-Injection
- SSRF-Angriffe
- Anmeldedaten-Exfiltration
- Bösartiges JavaScript
- Phishing-Muster
- Verschleierung (versteckter Code)

## Funktionen

### 🔍 4-Phasen-Audit-System

1. **Pre-Visit Scan** — URL vor Besuch prüfen
2. **Content Analysis** — Inhalte auf Bedrohungen analysieren
3. **Command Safety** — Befehle vor Ausführung validieren
4. **Self-Audit** — Periodische Selbstüberwachung

### 📊 216 Erkennungsmuster

Vollständiges Musterset basierend auf ClawGuard und OWASP Agentic AI Top 10.

## Installation

### Über OpenSkills (empfohlen)

```bash
# Repository klonen
git clone <repo-url> security-auditor-pro
cd security-auditor-pro

# Globale Installation
openskills install ./ --global
openskills sync --yes

# Oder lokale Installation
openskills install ./
openskills sync --yes
```

### Manuell

```bash
# Repository klonen
git clone <repo-url> security-auditor-pro

# Symbolischen Link erstellen
mkdir -p ~/.claude/skills
ln -s $(pwd)/security-auditor-pro ~/.claude/skills/security-auditor-pro
```

## Verwendung

### Schnellscan (ohne LLM)

```bash
./scripts/quick-scan.sh <pfad> [optionen]
```

### Vollständiger Scan (mit LM Studio)

```bash
./scripts/scan-skill-scanner.sh <pfad> [optionen]
```

## Kompatibilität

- ✅ OpenCode
- ✅ Claude Code (über OpenSkills)
- ✅ Cursor (über OpenSkills)
- ✅ Windsurf (über OpenSkills)
- ✅ OpenClaw
- ✅ Jeder Agent mit SKILL.md-Unterstützung

## Lizenz

MIT

## Version

1.1.0