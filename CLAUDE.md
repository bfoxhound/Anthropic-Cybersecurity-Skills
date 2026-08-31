# Anthropic-Cybersecurity-Skills

Community-maintained library of Claude Agent Skills for cybersecurity work
(816 skills across 29 security domains — offense, defense, forensics,
compliance — mapped to MITRE ATT&CK/F3, NIST CSF, and OWASP). Distributed as
a Claude Code plugin via `.claude-plugin/marketplace.json` +
`.claude-plugin/plugin.json`.

## Stack
- Markdown skill definitions under `skills/`, one directory per skill
- `mappings/` — MITRE ATT&CK, NIST CSF, OWASP crosswalks (JSON + Markdown)
- `tools/` — `validate-skill.py`, `validate-agentskills.py`,
  `agentskills-skill.schema.json` (Python, no committed dependency manifest)
- `.claude-plugin/` — Claude Code plugin marketplace manifest
- GitHub Actions: `validate-skills.yml`, `update-index.yml`,
  `sync-marketplace-version.yml`

## TODO for Jenny
- Confirm whether this fork/mirror under `bfoxhound` is meant to track
  upstream (`mukul975/Anthropic-Cybersecurity-Skills`) or diverge
  independently — affects whether future heal PRs here should stay minimal.
- This library documents offensive/dual-use techniques (red-team C2,
  phishing simulation) for authorized use per its own `SECURITY.md` — worth
  a read before treating any workflow failure here as purely mechanical.
