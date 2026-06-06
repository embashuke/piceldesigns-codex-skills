# Piceldesigns Codex Skills

Upload this folder to a GitHub repository, preserving the `skills/` directory.

## Folder Structure

```text
skills/
├── piceldesigns-build-control/
│   ├── SKILL.md
│   └── agents/
│       └── openai.yaml
└── piceldesigns-frontend-website-designer/
    ├── SKILL.md
    └── agents/
        └── openai.yaml
```

## Install From GitHub

Install both skills:

```bash
python3 /Users/user/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo embashuke/piceldesigns-codex-skills \
  --path skills/piceldesigns-build-control \
  --path skills/piceldesigns-frontend-website-designer
```

Install only the build-control skill:

```bash
python3 /Users/user/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo embashuke/piceldesigns-codex-skills \
  --path skills/piceldesigns-build-control
```

Restart Codex after installing new skills.
