# ka88-agent-shield

Auditoría de seguridad profesional para agentes de IA.

## Descripción

ka88-agent-shield es una habilidad para agentes de IA que proporciona protección integral contra:
- Inyección de Prompts (Prompt Injection)
- Ataques SSRF
- Filtración de Credenciales
- JavaScript Malicioso
- Patrones de Phishing
- Ofuscación de Código

## Características

### 🔍 Sistema de Auditoría de 4 Fases

1. **Pre-Visit Scan** — Verificar URL antes de visitar
2. **Content Analysis** — Analizar contenido en busca de amenazas
3. **Command Safety** — Validar comandos antes de ejecutarlos
4. **Self-Audit** — Auto-monitoreo periódico

### 📊 216 Patrones de Detección

Conjunto completo de patrones basado en ClawGuard y OWASP Agentic AI Top 10.

## Instalación

### Via OpenSkills (recomendado)

```bash
# Clonar repositorio
git clone <repo-url> security-auditor-pro
cd security-auditor-pro

# Instalación global
openskills install ./ --global
openskills sync --yes

# O instalación local
openskills install ./
openskills sync --yes
```

### Manual

```bash
# Clonar repositorio
git clone <repo-url> security-auditor-pro

# Crear enlace simbólico
mkdir -p ~/.claude/skills
ln -s $(pwd)/security-auditor-pro ~/.claude/skills/security-auditor-pro
```

## Uso

### Escaneo Rápido (sin LLM)

```bash
./scripts/quick-scan.sh <ruta> [opciones]
```

### Escaneo Completo (con LM Studio)

```bash
./scripts/scan-skill-scanner.sh <ruta> [opciones]
```

## Compatibilidad

- ✅ OpenCode
- ✅ Claude Code (vía OpenSkills)
- ✅ Cursor (vía OpenSkills)
- ✅ Windsurf (vía OpenSkills)
- ✅ OpenClaw
- ✅ Cualquier agente con soporte SKILL.md

## Licencia

MIT

## Versión

1.1.0