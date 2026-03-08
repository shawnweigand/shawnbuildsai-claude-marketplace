---
name: competitive-research
description: >
  This skill should be used when the user asks to "research my competitors",
  "check what competitors are doing", "give me a competitive digest",
  "weekly competitor update", "what's new with [company]", "competitor analysis",
  "market intel", "what are rivals doing", or provides a list of company names
  or URLs and asks for any kind of summary, analysis, or digest.
  Also triggers for "competitive intelligence", "track competitors", or
  "monitor competitors".
version: 0.1.0
---

# Competitive Intelligence Skill

Produce a structured weekly competitive intelligence digest for a list of competitors provided by the user. Research each company's recent activity, synthesize the findings, and deliver a digest with per-competitor sections followed by a cross-competitor comparison.

## Core Principles

- **Factual and neutral**: Report what is observed, not what is assumed. Do not editorialize. Do not exaggerate threats or opportunities.
- **Recent activity only**: Focus on content published or updated within approximately the last 7–14 days unless the user specifies a different window.
- **Signal over noise**: Surface changes that indicate strategic movement — new features, pricing shifts, content pivots, event announcements. Skip routine low-signal content.
- **Concise bullets**: Each finding is 1–2 sentences. The digest should be scannable, not a wall of text.

## Research Process

For each competitor provided, follow this sequence:

### 1. Identify the competitor's web presence
- Use the company name or URL the user provides.
- Visit their main website to confirm it's current and capture their homepage positioning (tagline, hero message, primary CTA).
- Note any changes to homepage messaging if it's been tracked before.

### 2. Gather recent content and updates
Research each of the following areas using web search and direct site visits:

**Blog posts & content**
- Search for recent articles, announcements, or news from the past 7–14 days.
- Identify the topic, publish date, and any notable angle or claim.
- Note if they've shifted content themes (e.g., from product-focused to thought leadership).

**Product updates & pricing changes**
- Check their product changelog, release notes page, or blog for "what's new" posts.
- Visit their pricing page and note tier names, prices, and any recent changes.
- Flag any new products, features, integrations, or deprecated offerings.

**Upcoming events**
- Search for webinars, conferences, product launches, or virtual events they've announced.
- Include event name, date, and brief description if available.

**Social media highlights**
- Search for recent notable posts on LinkedIn and Twitter/X.
- Focus on posts with high engagement, announcements, or content that signals positioning.
- Do not list routine low-engagement posts.

### 3. Evaluate significance
For each finding, ask: does this represent a meaningful strategic move? If yes, include it. If it's routine or low-signal, skip it. It's better to have 3 strong findings per competitor than 8 weak ones.

## Output Format

Produce the digest in this exact structure:

---

## 🔍 Competitive Intelligence Digest
*[Date range covered, e.g., "Week of March 3–9, 2026"]*

---

### [Competitor Name]
*[One-sentence description of what they do / their current positioning]*

**Recent Content & Blog Posts**
- [Finding 1: topic, date, key angle]
- [Finding 2]

**Product Updates & Pricing**
- [Finding 1: what changed, when, significance]
- [Finding 2]

**Upcoming Events**
- [Event name — date — brief description]
- *(None found in this period)* ← use this if nothing was found

**Social Media Highlights**
- [Platform — notable post or theme — engagement signal if notable]

---

*(Repeat the above block for each competitor)*

---

## 📊 Competitive Comparison

### Positioning Gaps
*What competitors are saying or emphasizing that you are not.*
- [Observation with implication]
- [Observation with implication]

### Feature Gaps
*Capabilities or offerings competitors have that may differ from yours.*
- [Observation with implication]
- [Observation with implication]

### Strategic Direction
*What their collective activity signals about where the market is heading.*
- [Pattern observed across competitors]
- [Pattern observed across competitors]

---

## Tone and Style Rules

- Write in third person about competitors ("Acme Corp announced…", not "they announced…").
- Use plain language. No jargon unless it's industry-standard.
- Dates should be specific when known ("March 5" not "recently").
- If information is unavailable or a section is empty, say so explicitly — do not fabricate.
- If a competitor's site is inaccessible or returns no results, note this and move on.
- Keep each competitor section to roughly 200–300 words. The full digest for 3 competitors should be under 1,200 words.

## Handling Edge Cases

- **No recent content found**: Write "No significant activity found in this period for [Competitor]." Do not pad with old content.
- **Paywalled or inaccessible content**: Note that the content exists but couldn't be accessed. Do not speculate on its contents.
- **User provides a URL instead of a name**: Use the URL to identify the company name, then proceed normally.
- **User asks for a specific competitor only**: Apply the same process to just that one company and produce a single-competitor report.

## Additional Reference

See `references/research-prompts.md` for search query templates to use when researching each section.
See `references/comparison-framework.md` for detailed guidance on writing the comparison section.
