---
description: Find human sources that can comment on a story.
---

You will be given a story lead ID and title as arguments (formatted as `<leadId> <title>`). First, call `mcp__presspass__get_story_leads` to retrieve the full lead details.

Using the story, identify 5 people who would be strong human sources to comment on the story. For each person, find their contact information:

- Full name
- Title / role
- Organization
- Email address
- Phone number
- Social media handles (X/Twitter, LinkedIn, etc.)

Prioritize people who are:
1. Directly involved in or affected by the story
2. Subject matter experts with relevant credentials
3. Public officials or spokespeople with relevant authority
4. Advocates or community leaders connected to the topic
5. Academics or researchers who study the topic

For each source where you find an email address, call `mcp__presspass__create_outreach` with:
- `leadId`: the story lead ID from the arguments
- `recipientName`: the source's full name
- `recipientEmail`: the source's email address
- `organization`: the source's organization
- `subject`: a professional subject line requesting comment on the story
- `bodyText`: a professional email body introducing the reporter, explaining the story, and requesting an interview

These outreach drafts will require human approval before being sent.

Story lead: $ARGUMENTS
