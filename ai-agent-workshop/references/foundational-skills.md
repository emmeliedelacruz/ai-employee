# Foundational Skills Reference

This file contains instructions for building foundational skills that apply to all AI employees.
Read this file before building the voice and tone skill. Prework Part 2 uses it.

---

## The Voice and Tone Skill

Every AI employee that interacts with external audiences needs a voice and tone skill. This skill
is built once and referenced by all external-facing employees. It does not get rebuilt for each
employee. If the attendee already has a voice and tone skill from a previous session, confirm it
is still accurate and update it if needed.

### What to extract from their writing samples

When the attendee pastes writing samples, analyze for these dimensions and document each one
explicitly in the skill. Do not leave any dimension vague.

**Sentence structure:** Are their sentences short and punchy or long and layered? Do they use
fragments for effect or always write complete sentences? Count average words per sentence across
the samples.

**Openings:** How do they start emails, messages, or posts? Do they get to the point immediately
or warm up first? Do they use greetings or skip them?

**Closings:** How do they end communication? Do they include a call to action, a question, a
next step, or just stop?

**Recurring phrases:** List specific phrases that appear more than once. These go into the skill
as phrases the employee should use naturally.

**Avoided patterns:** Note what never appears. If they never use exclamation points, that is a
rule. If they never say "hope this finds you well," that is a rule.

**Warmth level:** On a scale from purely transactional to highly relational, where do they land?
Do they acknowledge the person before the business or lead with the business?

**Directness:** Do they soften requests and feedback or deliver them plainly? Both are valid.
Document which one.

**Humor:** Do they use humor? What kind? Dry, self-deprecating, playful? Or none at all?

**Handling difficulty:** How do they write when delivering bad news, pushing back, or following
up on something overdue? Extract a pattern if samples exist.

### Voice and tone skill structure

Build the skill in this format:

```
---
name: voice-and-tone
description: >
  Use this skill for all written communication produced on behalf of [name]. This skill applies
  to every email, message, post, or document the AI employee writes for external audiences.
  Always reference this skill before writing anything that will be seen by a client, customer,
  or external partner.
---

# Voice and Tone for [Name]

## Who This Voice Belongs To

[Two to three sentences describing this person's communication style in plain language. Write
it like you are briefing a ghostwriter.]

## Sentence Structure

[Specific rules. Example: "Sentences average eight to twelve words. Long sentences exist but
are broken up by short ones immediately after. Never write three long sentences in a row."]

## How to Open

[Specific rules for how to start different types of communication. Cover email, follow-ups,
and any other formats relevant to their business.]

## How to Close

[Specific rules for endings. What is always included. What is never included.]

## Phrases to Use

[List actual phrases extracted from their samples. These should appear naturally in outputs.]
- [Phrase 1]
- [Phrase 2]
- [Add all identified]

## Phrases to Never Use

[List phrases that never appear in their writing or that conflict with their voice.]
- [Phrase 1]
- [Phrase 2]
- [Add all identified]

## Warmth and Directness

[Describe where they land and give a concrete example of how to apply it. Example: "Lead with
the business point. Acknowledge the person in one sentence maximum if the situation calls for
it. Do not warm up for more than one line before getting to the purpose of the message."]

## Handling Difficult Communication

[Rules for bad news, pushback, overdue follow-up, and complaints. If no samples exist for this,
note it and default to their general directness level.]

## Format Rules

[Any consistent formatting patterns: whether they use bullet points, whether they bold anything,
paragraph length, email signature style, etc.]

## What This Voice Never Does

[Hard negatives. Things that would immediately signal this is not them.]
- [Never 1]
- [Never 2]
```

### Testing the voice skill

After building it, run this test before moving on:

Scenario 1: "Write a follow-up email to a client who has not responded in five days."
Scenario 2: "Write a message to a client explaining that their project will be delayed by one week."

If the attendee says either output does not sound like them, ask specifically: "What word or
sentence felt wrong?" Update that dimension in the skill and retest. Do not move to Phase 3
until both scenarios pass.

---

## Internal Voice Default

For employees that interact only with internal teams, do not build a custom voice skill. Apply
these defaults directly in the system prompt:

- Write in complete sentences. No filler words.
- Lead with the action or decision. Context comes after if needed.
- No pleasantries unless the situation specifically calls for them.
- Bullet points for lists of three or more items.
- Flag urgency explicitly. Do not make the reader infer it.
- One idea per message. If more than one decision is needed, number them.
