# ai-marketing-claude

> **A marketing team in 12 Claude skills** - Skill pack that replaces a CMO, content lead, ads buyer, SEO analyst, and brand strategist - Claude Code native, file-system simple, agency-grade output.

<p align="center"><a href="https://github.com/hmzainjamil/ai-marketing-claude">Repository</a> · <a href="https://github.com/hmzainjamil/ai-marketing-claude/commits/main">Commits</a> · <a href="https://github.com/hmzainjamil/ai-marketing-claude/issues">Issues</a></p>
<p align="center"><img alt="Documentation" src="https://img.shields.io/badge/documentation-deep%20editorial-lightgrey"> <img alt="Lifecycle" src="https://img.shields.io/badge/lifecycle-active-success"></p>

<!-- HMZ DEEP README v1 -->

## At a glance

| Field | Current state |
|---|---|
| Repository | ai-marketing-claude |
| Visibility | Public |
| Lifecycle | Active |
| Evidence basis | Current repository documentation and source-visible material |

## Why this exists

**A marketing team in 12 Claude skills** - Skill pack that replaces a CMO, content lead, ads buyer, SEO analyst, and brand strategist - Claude Code native, file-system simple, agency-grade output.

The README documents the marketing workflow scope while separating skill definitions and automation behavior from claims about customer or campaign outcomes.

## CONCEPTS

| Concept | Location | Description |
|---|---|---|
| **Market master skill** | `market/SKILL.md` | Top-level marketing orchestrator - [Source](https://github.com/hmzainjamil/ai-marketing-claude/blob/main/market/SKILL.md) |
| **Ads skill** | `skills/market-ads/SKILL.md` | Headline + creative generator - [Source](https://github.com/hmzainjamil/ai-marketing-claude/blob/main/skills/market-ads/SKILL.md) |
| **Audit skill** | `skills/market-audit/SKILL.md` | 25-point teardown of any URL - [Source](https://github.com/hmzainjamil/ai-marketing-claude/blob/main/skills/market-audit/SKILL.md) |
| **Brand skill** | `skills/market-brand/SKILL.md` | Voice / tone / palette builder - [Source](https://github.com/hmzainjamil/ai-marketing-claude/blob/main/skills/market-brand/SKILL.md) |
| **Page analyzer** | `scripts/analyze_page.py` | Headless audit of a URL - [Source](https://github.com/hmzainjamil/ai-marketing-claude/blob/main/scripts/analyze_page.py) |
| **Competitor scanner** | `scripts/competitor_scanner.py` | Diffs 5 competitors on positioning - [Source](https://github.com/hmzainjamil/ai-marketing-claude/blob/main/scripts/competitor_scanner.py) |
| **Social calendar** | `scripts/social_calendar.py` | 30-day content plan generator - [Source](https://github.com/hmzainjamil/ai-marketing-claude/blob/main/scripts/social_calendar.py) |
| **PDF report** | `scripts/generate_pdf_report.py` | ReportLab branded audit PDF - [Source](https://github.com/hmzainjamil/ai-marketing-claude/blob/main/scripts/generate_pdf_report.py) |
| **Strategy agent** | `agents/market-strategy.md` | GTM + positioning agent - [Source](https://github.com/hmzainjamil/ai-marketing-claude/blob/main/agents/market-strategy.md) |
| **Conversion agent** | `agents/market-conversion.md` | CRO + funnel agent - [Source](https://github.com/hmzainjamil/ai-marketing-claude/blob/main/agents/market-conversion.md) |

## HOW IT WORKS

```
+---------------------------------------------------------+
|                       INPUT                             |
|   12 - ads, audit, brand, competitors, copy, emails,|
+--------------------------+------------------------------+
                           v
+---------------------------------------------------------+
|                  ORIENT / PARSE                         |
|   - Validate inputs                                     |
|   - Load skill / agent / tool definitions               |
|   - Resolve config + secrets from .env                  |
+--------------------------+------------------------------+
                           v
+---------------------------------------------------------+
|                  PLAN (Claude Sonnet)                   |
|   - Decompose goal into ordered subtasks                |
|   - Pick model per task (Sonnet / Haiku / Tier-0)       |
+--------------------------+------------------------------+
                           v
+---------------------------------------------------------+
|                  EXECUTE (parallel)                     |
|   - Spawn sub-agents / call tools                       |
|   - Stream tokens, persist artifacts                    |
+--------------------------+------------------------------+
                           v
+---------------------------------------------------------+
|                  VERIFY                                 |
|   - Lint / typecheck / visual diff / QA agent           |
|   - On failure -> re-prompt with error context          |
+--------------------------+------------------------------+
                           v
+---------------------------------------------------------+
|                  SHIP                                   |
|   - Write to disk . commit . PR . upload                |
+---------------------------------------------------------+
```

## Install

```bash
git clone https://github.com/hmzainjamil/ai-marketing-claude.git
cd ai-marketing-claude

# Per-repo install (try in order):
bash install.sh 2>/dev/null || \
npm install 2>/dev/null || \
bun install 2>/dev/null || \
pip install -r requirements.txt 2>/dev/null || true
```

Environment:

```bash
cp .env.example .env  # if present
# fill ANTHROPIC_API_KEY at minimum
```

## Usage

```bash
# Claude Code skill packs:
/skill-name "your goal"

# CLI / scripts:
python scripts/<script>.py --input ./input --output ./output

# TypeScript projects:
bun run dev    # or npm run dev
```

### Configuration knobs

| Key | Default | Description |
|---|---|---|
| `ANTHROPIC_API_KEY` | - (required) | Claude API key |
| `MODEL` | `claude-sonnet-4-7` | Default LLM |
| `MODEL_FALLBACK` | `claude-haiku-4` | Cheaper fallback |
| `MAX_TOKENS` | `8192` | Per-call ceiling |
| `TEMPERATURE` | `0.2` | Determinism dial |
| `LOG_LEVEL` | `info` | debug / info / warn / error |
| `OUT_DIR` | `./out` | Where artifacts land |
| `CACHE_DIR` | `.cache` | Prompt cache root |
| `PARALLELISM` | `4` | Sub-agent concurrency |
| `RETRY_MAX` | `3` | Per-call retry budget |
| `TIMEOUT_S` | `120` | Per-call timeout |
| `DRY_RUN` | `false` | Plan-only, no side effects |

### Case 3 - DTC brand, ad creative testing

- Before: $2K/month UGC creator retainer, 4 ads/month.
- After: 30+ ad variants/week via Arcads + Claude, A/B-tested.
- Result: 3x creative velocity, 41% lower CAC after 6 weeks.

## Security

- Never commit API keys. `.env` is in `.gitignore` by default.
- Use [git-secret](https://git-secret.io/) or 1Password CLI for team secret sharing.
- Review the QA / safety layer for any tool that writes to disk or runs shells (see `mac_safety.py` style guards).
- Vulnerability reports: open a private GitHub Security Advisory.

## Limitations

- External platform behavior and current model capabilities can change.
- Marketing outcomes depend on strategy, execution, audience, offer, and measurement.
- Quantitative performance claims require time-bounded evidence.

## Related

- [Claude Code](https://docs.claude.com/en/docs/claude-code) - official docs
- [Anthropic Console](https://console.anthropic.com) - API keys + billing
- [Crawlee](https://crawlee.dev) - web scraping framework
- [hmz-claude-code-best-practice](https://github.com/hmzainjamil/hmz-claude-code-best-practice) - sister repo

## Maintainer

[hmzainjamil](https://github.com/hmzainjamil)