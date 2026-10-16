# Voice Extraction Reference

Read this file before building the foundational voice and tone skill in Part 3 of prework.
Follow the full process below. Do not skip dimensions.

---

## What to Extract From Their Writing Samples

Analyze every sample before writing anything. Look for patterns across all of them, not just
one. Document each dimension explicitly. Vague descriptions produce vague outputs.

**Sentence length and rhythm**
Count average words per sentence. Note whether sentences vary in length or stay consistent.
If they use short sentences for emphasis after longer ones, document that pattern specifically.

**Openings**
How do they start? Do they get to the point immediately or warm up first? Do they use
greetings like "Hi [name]" or skip straight to the subject? Note any consistent opening phrases.

**Closings**
How do they end? Do they always include a next step, a question, or a call to action? Do they
sign off with something specific or just their name? Note the pattern exactly.

**Recurring phrases**
List every phrase that appears more than once across the samples. These belong in the skill
as phrases the AI employee should use naturally. Do not paraphrase them. Use the exact words.

**Avoided patterns**
Note what never appears. If exclamation points are absent, that is a rule. If "hope this finds
you well" never shows up, that is a rule. If they never start with "I," document it.

**Warmth level**
Where do they land between purely transactional and highly relational? Do they acknowledge the
person before the business or lead with the purpose of the message? Be specific. "Moderately
warm" is not specific. "Acknowledges the person in one sentence then moves to the point" is.

**Directness**
Do they soften requests and feedback or deliver them plainly? Do they use phrases like "I
wanted to reach out" (softened) or "I am following up on" (direct)? Document which pattern
dominates and whether exceptions exist.

**Humor**
Is humor present at all? If yes, what kind? Dry, self-deprecating, playful, or dry understatement?
If absent, note it as a hard rule: no humor unless the situation clearly calls for it.

**Handling difficulty**
If any samples involve bad news, follow-ups on overdue items, or pushback, extract the pattern.
How do they frame it? Do they lead with the problem or the solution? Do they apologize or just
state the situation? If no samples cover this, note it and default to their general directness.

---

## Skill Structure

Write the skill in this exact format after completing the extraction above.

```
---
name: voice-and-tone
description: >
  Use this skill for all written communication produced on behalf of [name]. Apply this skill
  to every email, message, post, or client-facing document. Always reference this skill before
  writing anything that will be seen by a client, customer, or external partner. Do not write
  external communication without consulting this skill first.
---

# Voice and Tone: [Name]

## Who This Voice Belongs To

[Two to three sentences describing this person's communication style in plain language.
Write it as if briefing a ghostwriter who has never met them.]

## Sentence Structure

[Specific rules with numbers where possible. Example: "Sentences average eight to twelve
words. Longer sentences exist but are always followed by a shorter one. Three long sentences
in a row never happen."]

## How to Open

[Specific rules by communication type. Cover email, follow-up messages, and any other
formats that appeared in their samples.]

## How to Close

[Specific rules. What is always included. What never appears.]

## Phrases to Use

These phrases appear naturally in this person's writing. Use them where they fit.
- [Exact phrase from samples]
- [Exact phrase from samples]
- [Add all identified]

## Phrases to Never Use

These phrases never appear and would signal this is not them.
- [Phrase 1]
- [Phrase 2]
- [Add all identified]

## Warmth and Directness

[One concrete paragraph describing where they land and how to apply it. Include a specific
example of how to open a message given their warmth level.]

## Handling Difficult Communication

[Rules for bad news, overdue follow-ups, pushback, and complaints. If no samples exist,
write: "No samples available for this. Default to [their general directness level] and
lead with the situation before the solution."]

## Format Rules

[Any consistent patterns: bullet point usage, paragraph length, whether they bold anything,
email signature style, use of line breaks.]

## What This Voice Never Does

- [Hard negative 1]
- [Hard negative 2]
- [Add all identified]
```

---

## Testing Standard

Both test scenarios must pass before the skill is confirmed complete.

Scenario 1: Follow-up to a client who has not responded in five days.
Scenario 2: Message to a client explaining a one-week project delay.

A passing output means the attendee reads it and says it sounds like them. If they say it is
close but something is off, ask them to identify the specific word, sentence, or pattern that
feels wrong. Update that dimension in the skill and retest. Do not accept "it's mostly fine."
The voice skill is foundational. Every AI employee they ever build will use it. It needs to
be right before the workshop starts.
