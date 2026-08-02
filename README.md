# Claude Skills

Random Claude skills i built :). Each one lives in its own folder with a `SKILL.md` that tells Claude when to use it and how.

## Structure

```
claude-skills/
├── README.md
├── skills/
|   ├── template/
|   │   └── blank-SKILL.md
|   └── larp-max/
|       └── larpmax-SKILL.md
|
├── prompts/
|   ├── template/
|   |    └── blank-prompt.md
|   |
... └── school/
        └──grad-gifts.md
```

Every skill lives under `skills/`, one folder each (compex skills have an "XSkill-explainer.md"). `~skills/template/` holds a blank `SKILL.md` to copy when starting a new one.

## Install

Copy a skill's folder into Claude's user skills directory:

```
/mnt/skills/user/<skill-name>/SKILL.md
```

Claude picks it up on its own once a request matches the skill's description. No need to name it directly.

## Skills

| Skill | What it does |
|---|---|
| [`larp-max`](./skills/larp-max/SKILL.md) | Turns plain descriptions of real work into résumé bullets, skills-section language, and cover letter copy.  |

More rows get added here as I build more skills.

## Adding a new skill

1. Copy `skills/_template/` to `skills/skill-name/`
2. Fill in `skill-name/SKILL.md`:
   - YAML frontmatter (`name`, `description`). Claude matches on the description, so it needs to be specific.
   - A `# Skill Name` header and short overview
   - `## When to Use This Skill`
   - `## Instructions`, the actual steps
   - `## Examples`, real input/output pairs
   - Any hard rules the skill has to hold to
3. Add a row to the table above
4. Copy the folder to `/mnt/skills/user/`