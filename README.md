# AI Marketing Claude

A Claude Code marketing skill pack with 15 workflow skills, five agent instruction files, four Python scripts, templates, and an installer. It provides prompt-guided analysis and content generation. It is not a hosted marketing service, ad platform integration, or measured campaign system.

## Included

| Component | Purpose |
|---|---|
| `market/SKILL.md` | Orchestrates the `/market` command set |
| `skills/` | Audit, copy, email, social, ads, funnel, competitor, landing, launch, proposal, report, SEO and brand workflows |
| `agents/` | Five role-specific analysis instructions |
| `scripts/analyze_page.py` | Fetches and parses page HTML |
| `scripts/competitor_scanner.py` | Fetches and parses competitor pages |
| `scripts/social_calendar.py` | Produces a structured content calendar |
| `scripts/generate_pdf_report.py` | Builds a report PDF with ReportLab |
| `templates/` | Content calendar, email, launch and proposal starting points |

The skill instructions may request web access and parallel subagents. Their availability depends on the configured Claude Code environment. Review the output and verify source evidence before using it for business decisions. Scores, legal observations, market claims and performance estimates are drafts, not validated results.

## Requirements

- Claude Code for the Markdown skills and agent instructions.
- Python 3 for the scripts.
- ReportLab, declared as an optional dependency in `requirements.txt`, for PDF generation.
- Network access for scripts that fetch website pages.

## Install

Review `install.sh` before running. It copies the orchestrator, skill instructions, agent files and scripts to `$HOME/.claude/skills` and `$HOME/.claude/agents`. Matching files can be overwritten. The installer also checks related suites and prints commands; review those URLs before use.

```bash
git clone https://github.com/hmzainjamil/ai-marketing-claude.git
cd ai-marketing-claude
bash install.sh
```

## Usage

Start a Claude Code session after installation. Commands defined in `market/SKILL.md` include:

```text
/market audit <url>
/market quick <url>
/market copy <url>
/market social <topic-or-url>
/market competitors <url>
/market report-pdf <url>
```

Each skill documents its own inputs and workflow. Do not provide confidential client data to AI providers or external tools unless approved for that use.

Generate a PDF from JSON data:

```bash
python3 scripts/generate_pdf_report.py input.json output.pdf
```

The script requires ReportLab and writes to the selected output path. The PDF content comes from the supplied JSON; inspect it before sharing.

## Uninstall

Review `uninstall.sh` first. It recursively removes named `market*` skill directories and five matching agent files under the Claude home directories. Back up local edits and inspect those paths before running:

```bash
bash uninstall.sh
```

## Limitations

- Skills are Markdown instructions; external capabilities depend on host tools and permissions.
- The page-fetching scripts make network requests to supplied URLs. Use only authorized targets and review output.
- No ad account connection or campaign execution interface is present in this repository.
- Marketing scores and recommendations are not independently validated.
- Example performance claims in prior README copy were not accompanied by source data and are omitted.
- No test suite or supported-platform matrix is declared.

## Repository map

- [Main orchestrator](market/SKILL.md)
- [Workflow skills](skills/)
- [Agent instructions](agents/)
- [Python scripts](scripts/)
- [Templates](templates/)
- [Security notes](SECURITY.md)
- [License](LICENSE)

## Contributing

Open an issue with the affected file, expected behavior, and a safe reproduction using synthetic or public data. Do not include credentials, private client data, or scraped personal information.

## Security and privacy

See [SECURITY.md](SECURITY.md) for installer, network access, and data handling guidance.

## License

MIT. See [LICENSE](LICENSE).
