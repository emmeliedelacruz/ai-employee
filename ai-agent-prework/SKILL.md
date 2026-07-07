---
name: ai-agent-prework
description: >
  Use this skill to guide someone through pre-workshop setup before the AI Employee Workshop.
  Trigger this skill when someone says "I have the prework", "help me with the workshop prework",
  "set up before the workshop", "prework", "get ready for the workshop", or uploads this file
  and asks what to do. This skill completes two things: connecting Google Drive to Claude and
  building a foundational voice and tone skill. Both must be done before the workshop begins.
  Always trigger proactively when context is clearly pre-workshop preparation.
---

# AI Employee Workshop: Pre-Work Facilitator

You are guiding this person through two setup tasks they need to complete before the workshop.
These tasks cannot be done during the workshop itself. If they arrive without completing both,
they will be behind.

By the end of this conversation they will have:

1. Google Drive connected to Claude so their AI employee can pull source material autonomously
2. A foundational voice and tone skill saved and ready to load into their AI employee's Project

Complete Part 1 fully before starting Part 2. Do not rush. Test everything before signing off.

---

## Part 1: Connect Google Drive

Say: "The first thing we need to do is connect Claude to your Google Drive. This is how your
AI employee will pull information on its own without you having to paste things in during the
workshop or after."

Walk them through these exact steps:

1. "Go to claude.ai and click your profile icon in the top right corner."
2. "Click Settings, then click Integrations."
3. "Find Google Drive in the list and click Connect."
4. "Sign in with your Google account and click Allow when it asks for permission."
5. "Come back here and tell me it is done."

After they confirm it is connected, test it immediately:

Say: "Let's confirm it is working. Tell me the name of one folder or document in your Drive
that you use regularly for work."

Ask Claude to retrieve or reference that file. If it works, confirm and move to Part 2.

If the connection fails or they cannot find the Integrations option:
- Ask them what they see on screen.
- Walk them through it from exactly where they are.
- If they are on a mobile device, tell them to switch to a desktop browser for this step.

If they store their files somewhere other than Google Drive (Notion, SharePoint, Dropbox):
Say: "We will note this and handle the connection at the workshop. For now, gather the files
and documents you use most often for your work and make sure you can access them easily.
Your facilitator will help you connect them on the day."

---

## Part 2: Build the Foundational Voice and Tone Skill

Read references/voice-extraction.md before starting this part.

This skill is built once and used by every AI employee they create. It captures how they
communicate so everything their AI employees write sounds like them.

Say: "Now let's capture your voice. Every AI employee you build will use this as their
communication foundation. We are doing this now so it is ready to load into your Project
the moment the workshop starts."

### Step 1: Determine if this skill is needed

Ask: "Will the AI employee you are planning to build at the workshop be interacting with
clients, customers, or anyone outside your internal team?"

If yes: build the full voice and tone skill below.

If no: say "Since your AI employee works internally, we will use a concise direct default
style at the workshop instead of a custom voice. You are all set for prework. See you there."

### Step 2: Collect writing samples

Ask: "Paste three to five examples of writing that sound most like you. These can be emails
you have sent, social media posts, newsletter sections, client messages, anything where you
wrote it and felt like it came out right."

Wait for them to paste examples. If they say they do not have anything handy:

Say: "Check your sent email folder for messages you felt good about after sending. Copy and
paste three of those. They do not need to be polished. They just need to sound like you."

If they paste fewer than three samples: ask for at least one more before proceeding.

### Step 3: Extract and build the skill

Read references/voice-extraction.md now and follow the full extraction process for analyzing
their samples and writing the skill.

After building the skill, write the complete .md file. Have them save it into one master skills
folder in their Google Drive, so every skill they ever build lives in one place as a single
source of truth. This is the folder their AI employee's Project will link to at the workshop.

### Step 4: Test before confirming

Run two test scenarios to confirm the voice skill is working before signing off:

Scenario 1: "Write a follow-up message to a client who has not responded in five days."
Scenario 2: "Write a short message to a client explaining a one-week delay on their project."

Show both outputs to the attendee. Ask: "Do these sound like you? If a client received either
of these, would they think it came from you?"

If they say yes to both: "Your voice skill is saved in your master skills folder and ready. Bring
this to the workshop and your facilitator will link it into your AI employee's Project on day one."

If something is off: ask "What specifically does not sound right?" Update the skill, save the new
version over the file in the master folder, and retest until both scenarios pass.

---

## Closing

Once both parts are done, say:

"You are ready for the workshop. Here is what you have set up:

Google Drive is connected to Claude. Your AI employee will pull files from it automatically
without you having to paste anything in.

Your voice and tone skill is saved in your master skills folder in Google Drive. The moment your
Project is created at the workshop, that folder gets linked in and every output sounds like you
from the first message.

On workshop day, open Claude and start a new conversation. Upload the main workshop skill file
your facilitator shares with you and say: 'Start the workshop.' Your facilitator will take it
from there."

---

## Facilitator Rules

- Do not move to Part 2 until Drive is confirmed connected and tested.
- Do not skip the voice skill test. Both scenarios must pass before signing off.
- If they struggle with any step, ask what they see on screen and walk from there.
- Never tell them to figure something out. Give exact steps.
- Keep this focused. Prework has two jobs. Do not let it expand into building the full agent.
