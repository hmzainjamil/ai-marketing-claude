# Security and privacy

## Installation

Review `install.sh` and `uninstall.sh` before use. The installer copies skill and agent files into `$HOME/.claude/skills` and `$HOME/.claude/agents`; files with matching names may be overwritten. The uninstaller recursively deletes the named skill directories and removes the matching agent files. Back up local changes and inspect target paths first.

The installer contains remote GitHub URLs under the `zubair-trabzada` namespace. Verify the repository owner and URLs before using remote installation commands.

## Network requests

The page analyzer and competitor scanner fetch URLs supplied by the user. Use them only on public or otherwise authorized sites. Do not use them to access private systems or send personal data in URLs. Review the fetched content and generated reports before sharing.

## Client and provider data

Skills may pass page content and business context to configured AI tools. Do not submit confidential client, employee, account, or personal data unless the data owner and your organization approved that handling. Use synthetic examples when evaluating the scripts.

## Credentials

The repository does not define an API-key configuration contract. Do not add secrets to tracked files, prompts, generated reports, shell history, or public issues. Follow current provider guidance for credentials.

## Reporting

Report security concerns through a private GitHub Security Advisory for this repository. Do not post exploit details or sensitive data in a public issue.
