# ai-marketing-claude

> **AI marketing with Claude — campaign strategy, copy, and performance analysis**

![Status](https://img.shields.io/badge/status-active-brightgreen?style=flat)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat)
![Claude Code](https://img.shields.io/badge/Claude_Code-Skill-FF6B35?style=flat)
![Stars](https://img.shields.io/github/stars/hmzainjamil/ai-marketing-claude?style=flat)
![Last Commit](https://img.shields.io/github/last-commit/hmzainjamil/ai-marketing-claude?style=flat)

---

## CONCEPTS

| Concept | Description |
|---|---|
| **Campaign Strategy** | Full funnel planning from awareness to conversion |
| **Ad Copy** | Platform-specific copy for Meta, Google, LinkedIn |
| **Email Sequence** | Welcome, nurture, and conversion email chains |
| **SEO Content** | Keyword-optimized blog and landing pages |
| **Analytics** | Performance report interpretation and insights |
| **A/B Testing** | Hypothesis and variant generation |
| **Persona** | ICP development and messaging matrix |
| **Calendar** | Content calendar and scheduling logic |

---

## 🔥 Hot Commands

```bash
# Activate skill
claude --skill ai-marketing-claude 'your task'

# Quick workflow
claude 'marketing automation task'

# Get capabilities
claude 'what can ai-marketing-claude do?'
```

## ■ tip
> Mention **marketing** or **claude** in your prompt to auto-activate this skill.

---

## ☠️ STARTUPS / BUSINESSES

- **Agencies**: automate marketing workflows for clients at scale
- **Founders**: ship claude features 10x faster
- **Freelancers**: deliver campaign work with AI precision

---

## Features

- Marketing automation
- Claude automation
- Campaign automation
- Copy automation
- Ads automation
- Strategy automation

---

## Installation

```bash
git clone https://github.com/hmzainjamil/ai-marketing-claude.git
cd ai-marketing-claude
```

---

## Usage

```bash
# Activate skill in Claude Code
claude --skill ai-marketing-claude "your task here"

# Quick workflow
claude "marketing automation task"

# Get help
claude "what can ai-marketing-claude do?"
```

---

## Configuration

| Variable | Description | Default |
|---|---|---|
| `API_KEY` | Primary API key | Required |
| `MODEL` | AI model to use | claude-3-5-sonnet |
| `DEBUG` | Enable verbose debug | false |
| `MAX_TOKENS` | Max token budget | 8192 |
| `TIMEOUT` | Request timeout (sec) | 30 |
| `LOG_LEVEL` | Logging verbosity | info |

---

## Architecture

```
ai-marketing-claude/
├── README.md           # Documentation
├── SKILL.md            # Claude Code skill definition
├── scripts/            # Automation scripts
├── templates/          # Output templates
├── examples/           # Usage examples
└── docs/               # Extended documentation
```

---

## Examples

### Basic

```bash
# Simple task
claude --skill ai-marketing-claude "marketing task"

# Verbose
claude --skill ai-marketing-claude --verbose "detailed claude task"
```

### Advanced Pipeline

```bash
# Chain skills
claude --skill ai-marketing-claude "step 1" | claude --skill summarize

# Batch run
for item in $(cat list.txt); do
  claude --skill ai-marketing-claude "process $item"
done
```

---

## Troubleshooting

| Issue | Cause | Fix |
|---|---|---|
| Auth fails | Invalid API key | Re-export key in shell profile |
| Timeout | Network or large payload | Increase TIMEOUT value |
| Empty output | Prompt too vague | Add more context |
| Rate limit | Too many requests | Add delay between calls |
| Model error | Unsupported version | Update MODEL variable |
| Import error | Missing dependency | Run pip install -r requirements.txt |

---

## Comparison

| Feature | This Skill | Alt A | Alt B |
|---|---|---|---|
| Claude Code native | ✅ | ❌ | ✅ |
| Auto-activation | ✅ | ✅ | ❌ |
| Free to use | ✅ | ❌ | ✅ |
| Production ready | ✅ | ✅ | ❌ |
| Active maintenance | ✅ | ❌ | ❌ |

---

## Changelog

| Version | Changes |
|---|---|
| v2.0 | Claude 4 support, auto-activation |
| v1.5 | Added keyword triggers |
| v1.0 | Initial release |

---

## Contributing

1. Fork → feature branch → commit → PR
2. Follow conventional commits: `feat:`, `fix:`, `docs:`
3. Add tests for new features

---

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=hmzainjamil/ai-marketing-claude&type=Date)](https://star-history.com/#hmzainjamil/ai-marketing-claude&Date)

---

## 📜 License

MIT — free to use, modify, distribute.

---

Made with ❤️ by [@hmzainjamil](https://github.com/hmzainjamil)
