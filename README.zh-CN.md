# ka88-agent-shield

AI 代理专业安全审计工具。

## 描述

ka88-agent-shield 是面向 AI 代理的技能，提供全面保护：
- 提示词注入 (Prompt Injection)
- SSRF 攻击
- 凭证泄露 (Credential Exfiltration)
- 恶意 JavaScript
- 网络钓鱼模式
- 代码混淆 (Obfuscation)

## 功能

### 🔍 四阶段审计系统

1. **Pre-Visit Scan** — 访问前检查 URL
2. **Content Analysis** — 分析内容威胁
3. **Command Safety** — 执行前验证命令
4. **Self-Audit** — 定期自我监控

### 📊 216 个检测模式

基于 ClawGuard 和 OWASP Agentic AI Top 10 的完整模式集。

## 安装

### 通过 OpenSkills（推荐）

```bash
# 克隆仓库
git clone <repo-url> security-auditor-pro
cd security-auditor-pro

# 全局安装
openskills install ./ --global
openskills sync --yes

# 或本地安装
openskills install ./
openskills sync --yes
```

### 手动安装

```bash
# 克隆仓库
git clone <repo-url> security-auditor-pro

# 创建符号链接
mkdir -p ~/.claude/skills
ln -s $(pwd)/security-auditor-pro ~/.claude/skills/security-auditor-pro
```

## 使用

### 快速扫描（无需 LLM）

```bash
./scripts/quick-scan.sh <路径> [选项]
```

### 完整扫描（需要 LM Studio）

```bash
./scripts/scan-skill-scanner.sh <路径> [选项]
```

## 兼容性

- ✅ OpenCode
- ✅ Claude Code (通过 OpenSkills)
- ✅ Cursor (通过 OpenSkills)
- ✅ Windsurf (通过 OpenSkills)
- ✅ OpenClaw
- ✅ 任何支持 SKILL.md 的代理

## 许可证

MIT

## 版本

1.1.0