# Security Auditor Pro

Auditoria de segurança profissional para agentes de IA.

## Descrição

Security Auditor Pro é uma habilidade para agentes de IA que fornece proteção abrangente contra:
- Injeção de Prompts (Prompt Injection)
- Ataques SSRF
- Exfiltração de Credenciais
- JavaScript Malicioso
- Padrões de Phishing
- Ofuscação (código oculto)

## Recursos

### 🔍 Sistema de Auditoria em 4 Fases

1. **Pre-Visit Scan** — Verificar URL antes de visitar
2. **Content Analysis** — Analisar conteúdo para ameaças
3. **Command Safety** — Validar comandos antes da execução
4. **Self-Audit** — Auto-monitoramento periódico

### 📊 216 Padrões de Detecção

Conjunto completo de padrões baseado em ClawGuard e OWASP Agentic AI Top 10.

## Instalação

### Via OpenSkills (recomendado)

```bash
# Clonar repositório
git clone <repo-url> security-auditor-pro
cd security-auditor-pro

# Instalação global
openskills install ./ --global
openskills sync --yes

# Ou instalação local
openskills install ./
openskills sync --yes
```

### Manual

```bash
# Clonar repositório
git clone <repo-url> security-auditor-pro

# Criar link simbólico
mkdir -p ~/.claude/skills
ln -s $(pwd)/security-auditor-pro ~/.claude/skills/security-auditor-pro
```

## Uso

### Scan Rápido (sem LLM)

```bash
./scripts/quick-scan.sh <caminho> [opções]
```

### Scan Completo (com LM Studio)

```bash
./scripts/scan-skill-scanner.sh <caminho> [opções]
```

## Compatibilidade

- ✅ OpenCode
- ✅ Claude Code (via OpenSkills)
- ✅ Cursor (via OpenSkills)
- ✅ Windsurf (via OpenSkills)
- ✅ OpenClaw
- ✅ Qualquer agente com suporte SKILL.md

## Licença

MIT

## Versão

1.1.0