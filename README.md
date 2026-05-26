# codex-video-skills

Personal Codex skills for video workflows.

## Repository layout

```text
skills/
  <skill-name>/
    SKILL.md
    agents/
      openai.yaml
    scripts/
    references/
    assets/
```

Only `SKILL.md` is required for a skill. The other folders are optional:

- `agents/openai.yaml`: UI metadata for Codex skill lists and chips.
- `scripts/`: reusable executable helpers.
- `references/`: documentation Codex should load only when needed.
- `assets/`: templates, images, fonts, or other files used in generated output.

## Install a skill from this repo

Ask Codex:

```text
Install the Codex skill from https://github.com/jianghuancn/codex-video-skills/tree/main/skills/<skill-name>
```

Restart Codex after installing new skills.

