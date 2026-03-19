---
description: Enrich all story leads by running discovery skills against each story in parallel.
---

List all story directories in `skill-output/stories/`. Each directory contains a `pitch.md` created by the generate-story-leads skill.

For each story directory, run the following skills as parallel background subagents:

1. `/journalism-skills:trusted-human-source-discovery <story-directory-path>`
2. `/journalism-skills:find-photo-evidence <story-directory-path>`
3. `/journalism-skills:identify-new-questions-from-article <story-directory-path>`

Wait for all subagents to complete. Then summarize which stories were enriched and any that failed.
