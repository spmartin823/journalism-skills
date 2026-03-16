---
description: Create a new skill by asking the user questions and generating a SKILL.md template.
---

You are helping the user create a new skill. Ask the following questions one at a time, waiting for the user's response before proceeding:

1. **What should the skill be called?** (This will be the directory name, kebab-cased.)
2. **What should this skill do?** (A short description of its purpose.)
3. **What instructions should the skill give to Claude?** (The prompt body — what should Claude do when this skill is invoked?)
4. **Does the skill need arguments from the user?** (If yes, where should `$ARGUMENTS` be used in the prompt?)

Once you have all the answers, create the skill directory and SKILL.md file inside the `skills/` directory of the journalism-skills plugin. The generated SKILL.md should follow this format:

```markdown
---
description: <the description from question 2>
---

<the instructions from question 3, incorporating $ARGUMENTS if applicable>
```

After creating the file, confirm the skill name and how to invoke it (e.g., `/journalism-skills:skill-name`).
