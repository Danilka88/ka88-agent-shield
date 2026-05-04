# ka88-agent-shield

تدقيق أمني احترافي لوكلاء الذكاء الاصطناعي.

## الوصف

ka88-agent-shield هي مهارة لوكلاء الذكاء الاصطناعي توفر حماية شاملة ضد:
- حقن المطالبات (Prompt Injection)
- هجمات SSRF
- تسرب بيانات الاعتماد
- جافا سكريبت ضار
- أنماط التصيد
- التشويش (الرمز المخفي)

## الميزات

### 🔍 نظام التدقيق من 4 مراحل

1. **Pre-Visit Scan** - فحص عنوان URL قبل الزيارة
2. **Content Analysis** - تحليل المحتوى للتهديدات
3. **Command Safety** - التحقق من الأوامر قبل التنفيذ
4. **Self-Audit** - المراقبة الذاتية الدورية

### 📊 216 نمط الكشف

مجموعة كاملة من الأنماط مبنية على ClawGuard و OWASP Agentic AI Top 10.

## التثبيت

### عبر OpenSkills (موصى به)

```bash
# استنساخ المستودع
git clone <repo-url> security-auditor-pro
cd security-auditor-pro

# التثبيت العام
openskills install ./ --global
openskills sync --yes

# أو التثبيت المحلي
openskills install ./
openskills sync --yes
```

### يدوي

```bash
# استنساخ المستودع
git clone <repo-url> security-auditor-pro

# إنشاء رابط رمزي
mkdir -p ~/.claude/skills
ln -s $(pwd)/security-auditor-pro ~/.claude/skills/security-auditor-pro
```

## الاستخدام

### مسح سريع (بدون LLM)

```bash
./scripts/quick-scan.sh <المسار> [الخيارات]
```

### مسح كامل (مع LM Studio)

```bash
./scripts/scan-skill-scanner.sh <المسار> [الخيارات]
```

## التوافق

- ✅ OpenCode
- ✅ Claude Code (عبر OpenSkills)
- ✅ Cursor (عبر OpenSkills)
- ✅ Windsurf (عبر OpenSkills)
- ✅ OpenClaw
- ✅ أي وكيل يدعم SKILL.md

## الترخيص

MIT

## الإصدار

1.1.0