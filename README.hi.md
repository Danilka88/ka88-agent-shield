# Security Auditor Pro

AI एजेंट्स के लिए पेशेवर सुरक्षा ऑडिट।

## विवरण

Security Auditor Pro AI एजेंट्स के लिए एक स्किल है जो व्यापक सुरक्षा प्रदान करती है:
- प्रॉम्प्ट इंजेक्शन (Prompt Injection)
- SSRF हमले
- क्रेडेंशियल एक्सफिल्ट्रेशन (Credential Exfiltration)
- मैलिशियस जावास्क्रिप्ट
- फिशिंग पैटर्न
- ऑब्फुस्केशन (छिपा कोड)

## सुविधाएं

### 🔍 4-चरण ऑडिट सिस्टम

1. **Pre-Visit Scan** — विजिट करने से पहले URL जांचें
2. **Content Analysis** — खतरों के लिए सामग्री का विश्लेषण करें
3. **Command Safety** — निष्पादन से पहले कमांड सत्यापित करें
4. **Self-Audit** — आवधिक आत्म-निगरानी

### 📊 216 डिटेक्शन पैटर्न

ClawGuard और OWASP Agentic AI Top 10 पर आधारित पूर्ण पैटर्न सेट।

## स्थापना

### OpenSkills के माध्यम से (अनुशंसित)

```bash
# रेपो क्लोन करें
git clone <repo-url> security-auditor-pro
cd security-auditor-pro

# वैश्विक स्थापना
openskills install ./ --global
openskills sync --yes

# या स्थानीय स्थापना
openskills install ./
openskills sync --yes
```

### मैन्युअल

```bash
# रेपो क्लोन करें
git clone <repo-url> security-auditor-pro

# सिम्बोलिक लिंक बनाएं
mkdir -p ~/.claude/skills
ln -s $(pwd)/security-auditor-pro ~/.claude/skills/security-auditor-pro
```

## उपयोग

### त्वरित स्कैन (बिना LLM)

```bash
./scripts/quick-scan.sh <पथ> [विकल्प]
```

### पूर्ण स्कैन (LM Studio के साथ)

```bash
./scripts/scan-skill-scanner.sh <पथ> [विकल्प]
```

## संगतता

- ✅ OpenCode
- ✅ Claude Code (OpenSkills के माध्यम से)
- ✅ Cursor (OpenSkills के माध्यम से)
- ✅ Windsurf (OpenSkills के माध्यम से)
- ✅ OpenClaw
- ✅ कोई भी SKILL.md समर्थन वाला एजेंट

## लाइसेंस

MIT

## संस्करण

1.1.0