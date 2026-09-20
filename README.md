# Claude Skills

Random Claude skills i built :). Each one lives in its own folder with a `SKILL.md` that tells Claude when to use it and how.

## Structure

```
claude-skills/
├── README.md
|  
├── skills/
|   ├── template/
|   │   └── blank-SKILL.md
|   └── larp-max/
|       └── larpmax-SKILL.md
|
├── prompts/
|   ├── template/
|   |    └── blank-prompt.md
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
| [`larp-max`](./skills/larp-max/larpmax-SKILL.md) | Turns plain descriptions of real work into résumé bullets, skills-section language, and cover letter copy — exaggerates tone and framing, never fabricates facts. |
| [`ASD-STE100`](./skills/ASD-STE100/ASD-STE100-SKILL.md) | Rewrites text in ASD-STE100 Simplified Technical English. Explicit-invocation only (`/ste` or "use the ste skill") — won't fire on paraphrases like "simplify this." |
| [`study-guide`](./skills/study-guide/study-guide-SKILL.md) | Expands a basic study guide into an intensive, exam-ready reference doc built for use during open-note/open-book exams. |
| [`work-skills/Build-my-CV`](./skills/Build-my-CV/build-my-CV-SKILL.md) | Generates a personalized cover letter from a resume and job description. |
| [`work-skills/Work-email-writer`](./skills/Work-email-writer/work-email-writer-SKILL.md) | Drafts specific, human cold outreach emails to hiring managers and founders. |
| [`work-skills/Resume-Build-V2`](./skills/Resume-Build-V2/Resume-Build-v2-SKILL.md) | Builds targeted resume sections (summary, skills, experience) tailored to role and experience level. |


## Creating a new skill

1. Copy `skills/template/` to `skills/skill-name/`
2. Fill in `skill-name/SKILL.md`:
   - YAML frontmatter (`name`, `description`). Claude matches on the description, so it needs to be specific.
   - A `# Skill Name` header and short overview
   - `## When to Use This Skill`
   - `## Instructions`, the actual steps
   - `## Examples`, real input/output pairs
   - Any hard rules the skill has to hold to
3. Add a row to the table above
4. Copy the folder to `/mnt/skills/user/`

### Optional: Submit Pull Request

If the skill might be useful to others, open a PR:

1. Fork the repo and push your `skills/skill-name/` folder on a branch (separate from `main`)
2. Make sure `SKILL.md` frontmatter is filled in and the folder doesn't include stray files (like `.DS_Store`)
3. Open a PR against `main` with a short description of what the skill does and when it triggers
4. Tag it with a one-line summary in the PR title, e.g. `Add skill: skill-name`

Please try to keep it self-contained and make sure the description in the frontmatter is specific enough that Claude won't misfire on unrelated requests.
