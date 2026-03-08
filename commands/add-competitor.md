---
description: Quick single-competitor intelligence lookup
allowed-tools: WebSearch, WebFetch
argument-hint: [competitor name or URL]
---

The user wants a quick intelligence report on a single competitor: $ARGUMENTS.

Apply the competitive-research skill to research $ARGUMENTS. If no competitor is specified, ask: "Which competitor would you like me to look up?"

Produce a focused single-competitor report with the same four sections used in the full digest:
- Recent blog posts & content
- Product updates & pricing changes
- Upcoming events
- Social media highlights

Format the output as a standalone competitor section (same structure as one block from the full /competitive-research digest), without a comparison section.

Keep the report concise — aim for 150–250 words. If the user wants a full multi-competitor digest with a comparison section, suggest they use /competitive-research instead.
