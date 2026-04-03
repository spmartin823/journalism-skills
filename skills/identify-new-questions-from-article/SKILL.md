---
description: Read a story pitch and identify questions it does not yet address.
---

You will be given a story lead ID and title as arguments (formatted as `<leadId> <title>`). First, call `mcp__presspass__get_story_leads` to retrieve the full lead details including its existing questions.

In a good article, who, what, where, why, and how are all answered. Oftentimes when writing an article, some of these questions will be left unanswered. Read the lead and identify if any of these questions are unanswered.

For each unanswered question:

1. Identify which of the five W's (who, what, where, why, how) it falls under
2. State the specific question that remains unanswered
3. Research the answer using available tools

After identifying and researching all unanswered questions, call `mcp__presspass__add_question` for each new question with:
- `leadId`: the story lead ID from the arguments
- `questionText`: the question
- `questionType`: one of "who", "what", "where", "why", "how"

Story lead: $ARGUMENTS
