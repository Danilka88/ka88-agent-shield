# ka88-agent-shield

Профессиональный аудит безопасности для AI агентов.

## Описание

ka88-agent-shield — это навык (skill) для AI агентов, обеспечивающий комплексную защиту от угроз:
- Prompt Injection (внедрение промптов)
- SSRF атаки
- Credential Exfiltration (утечка учетных данных)
- Вредоносный JavaScript
- Фишинговые паттерны
- Обфускация (скрытый код)

## Возможности

### 🔍 4-фазная система аудита

1. **Pre-Visit Scan** — Проверка URL перед посещением
2. **Content Analysis** — Анализ контента на угрозы
3. **Command Safety** — Проверка команд перед выполнением
4. **Self-Audit** — Периодический самоконтроль

### 📊 216 Detection Patterns

Полный набор паттернов для обнаружения угроз, основанный на ClawGuard и OWASP Agentic AI Top 10.

### 🔧 Инструменты

| Скрипт | Описание | Требования |
|--------|----------|------------|
| `quick-scan.sh` | Быстрый скан без LLM | Только bash/grep |
| `scan-skill-scanner.sh` | Полный скан с LLM | skill-scanner + LM Studio |

## Установка

### Через OpenSkills (рекомендуется)

```bash
# Клонируй репозиторий
git clone <repo-url> security-auditor-pro
cd security-auditor-pro

# Глобальная установка
openskills install ./ --global
openskills sync --yes

# Или локальная установка
openskills install ./
openskills sync --yes
```

### Вручную

```bash
# Клонируй репозиторий
git clone <repo-url> security-auditor-pro

# Создай символическую ссылку
mkdir -p ~/.claude/skills
ln -s $(pwd)/security-auditor-pro ~/.claude/skills/security-auditor-pro
```

## Использование

### Активация

Навык активируется автоматически когда агент:
- Посещает веб-сайты
- Анализирует контент с URL
- Выполняет команды (curl, wget, pip, npm)
- Обрабатывает HTML/JS/CSS

### Быстрый скан (без LLM)

```bash
./scripts/quick-scan.sh <path> [options]

Options:
  --dry-run    Тестовый запуск (проверка конфигурации)
  --verbose    Подробный вывод
  --help       Показать справку

Examples:
  ./scripts/quick-scan.sh ./src
  ./scripts/quick-scan.sh ./src --verbose
  ./scripts/quick-scan.sh ./src --dry-run
```

### Полный скан (с LM Studio)

```bash
./scripts/scan-skill-scanner.sh <path> [options]

Options:
  --install    Установить skill-scanner если отсутствует
  --force      Использовать даже без LLM
  --help       Показать справку

Examples:
  ./scripts/scan-skill-scanner.sh ./my-skill
  ./scripts/scan-skill-scanner.sh ./my-skill --install
```

### Environment Variables

```bash
# LM Studio
LM_STUDIO_URL=http://localhost:1234/v1
MODEL=qwen3-35b-a3b

# Ограничения
MAX_FILES=1000
MAX_FILE_SIZE=10485760
MAX_SCAN_TIME=300

# Отладка
DEBUG=1

# Пути
VENV_PATH=/path/to/.venv

# Смотри также: config/env.example
```

### Конфигурация

Скопируй `config/env.example` в `.env` и настрой под себя:

```bash
cp config/env.example .env
# Отредактируй .env
```

## Требования

| Компонент | Для чего | Статус |
|-----------|----------|--------|
| bash + grep | quick-scan | Обязательно |
| Python 3.10+ | skill-scanner | Опционально |
| LM Studio + модель | LLM анализ | Опционально |

## Структура проекта

```
security-auditor-pro/
├── SKILL.md                    # Главный skill файл
├── .gitignore                  # Git исключения
├── README.md                   # English документация
├── README.ru.md                # Русская документация
├── README.*.md                 # Переводы на другие языки
├── config/
│   ├── patterns.yaml           # 216 паттернов
│   ├── ssrf-blocklist.yaml     # SSRF blocklist
│   └── env.example             # Шаблон конфигурации
├── scripts/
│   ├── quick-scan.sh           # Быстрый скан (без LLM)
│   └── scan-skill-scanner.sh   # Полный скан с LLM
├── procedures/
│   ├── 01-pre-visit.md         # Фаза 1: Pre-Visit Scan
│   ├── 02-content-analysis.md # Фаза 2: Content Analysis
│   ├── 03-commands.md          # Фаза 3: Command Safety
│   └── 04-self-audit.md        # Фаза 4: Self-Audit
└── templates/
    ├── finding.md             # Шаблон finding
    └── report.md              # Шаблон отчета
```

## Совместимость

- ✅ OpenCode
- ✅ Claude Code (через OpenSkills)
- ✅ Cursor (через OpenSkills)
- ✅ Windsurf (через OpenSkills)
- ✅ OpenClaw
- ✅ Любой агент с поддержкой SKILL.md

## Troubleshooting

### LM Studio недоступен

```
[ERROR] LM Studio недоступен
Убедись что:
1. LM Studio запущен
2. Модель загружена в память
3. Server включен в Developer tab
```

**Решение:** Скрипт автоматически переключится на quick-scan

### skill-scanner не установлен

```bash
# Вариант 1: Установить вручную
pip install cisco-ai-skill-scanner

# Вариант 2: Автоматически при запуске
./scripts/scan-skill-scanner.sh ./src --install
```

### Quick-scan ничего не находит

- Проверь что передаёшь правильный путь
- Попробуй с --verbose для подробного вывода

## Лицензия

MIT

## Версия

1.1.0

## Ссылки

- [Anthropic Agent Skills Spec](https://openagentskills.dev)
- [OpenSkills](https://github.com/numman-ali/openskills)
- [ClawGuard](https://github.com/joergmichno/clawguard)
- [skill-scanner](https://github.com/cisco-ai-defense/skill-scanner)
- [OWASP Agentic AI Top 10](https://owasp.org/www-project-agentic-ai-top-10/)