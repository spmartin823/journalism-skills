---
description: Find story leads by analyzing available sources for timely, outlier-driven local news. Takes a comma-separated list of zip codes to search.
---

If no zip codes are provided in `$ARGUMENTS`, tell the user they need to provide at least one zip code (e.g. `/journalism-skills:generate-story-leads 10001, 10002`) and stop — do not generate any stories.

You will be given a comma-separated list of zip codes. Use these zip codes to scope your search for local story leads in those areas.

Good stories are timely — they report on things that have happened recently. They also typically discuss outliers — a building that has received a ton of complaints, a cop that is paid extremely high, or a business that is opening in a space that hasn't been occupied in a long time for example.

Take a look at the available sources and try to find story leads relevant to the provided zip codes.

For each lead you discover, call the `mcp__presspass__create_story_lead` tool with:
- `title`: the headline
- `zipCode`: the zip code this story is relevant to
- `sourcesJson`: array of source description strings
- `questionsJson`: array of question strings the story asks
- `whyItMatters`: why this story matters to locals
- `importanceScore`: a subjective score 0-9 of how important you think the story is

Generate 10-20 leads per invocation.

Zip codes to search: $ARGUMENTS
