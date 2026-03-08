---
description: Run a weekly competitive intelligence digest
allowed-tools: WebSearch, WebFetch
argument-hint: [competitor1, competitor2, ...] or [competitor URLs]
---

The user wants a competitive intelligence digest for the competitors listed in $ARGUMENTS.

Parse $ARGUMENTS as a comma-separated or space-separated list of competitor names or URLs. If no arguments are provided, ask the user: "Which competitors would you like me to research? You can provide names (e.g., Acme Corp, Notion) or website URLs."

Once you have the competitor list:

1. Apply the competitive-research skill to conduct research on each competitor.
2. For each competitor, research:
   - Recent blog posts and content (last 7–14 days)
   - Product updates and pricing changes
   - Upcoming events or announcements
   - Notable social media activity (LinkedIn, Twitter/X)
3. After researching all competitors, produce the full digest following the output format defined in the skill, including:
   - A dated header
   - One section per competitor with findings under each category
   - A final comparison section covering positioning gaps, feature gaps, and strategic direction
4. Keep the tone factual and neutral throughout. Do not editorialize.
5. If a section has no findings, note it explicitly rather than leaving it blank or fabricating content.

Deliver the complete digest in the chat as formatted markdown.
