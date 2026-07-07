# How to Build Your First AI Employee
### A Setup Guide for Workshop Attendees

This guide walks you through everything you need to do before and during the workshop. Read it once before you start. Then follow each step in order.

You will end the workshop with a working AI employee inside Claude that handles one role in your business from start to finish.

---

## What You Need Before Starting

- A Claude account (claude.ai). You need a paid plan (Pro or higher) to use Projects and upload files.
- A Google account with Google Drive. This is how your AI employee pulls your files automatically.
- A scheduling tool, if any of your employee's tasks repeat on a schedule. A Claude Project cannot trigger itself, so recurring runs need either Claude Cowork (the /schedule command in the Claude Desktop app) or the Claude in Chrome extension (save a shortcut, then schedule it with the clock icon). You will install and set up one of these during the workshop's setup step. Both only run while your computer is awake and the app or browser is open.

---

## How This Works: Projects Are Employees, Skills Are How You Train Them

Before you build anything, understand the model. It makes every step after this click.

**A Claude Project is an AI employee.** The Project holds who that employee is (their instructions), what they can see (connected Google Drive folders), and how they do their work (their skills). You build one Project per employee.

**Skills are how you train that employee.** Each skill is one process written down as a file — how to run your weekly report, how to onboard a client, how to answer a common email. An employee has several skills linked to it inside its Project. Add a skill and the employee can do a new thing. Update a skill and the employee gets better at it.

**Skills are just files — `.md` or `.txt`.** A `.txt` file works if you only want to paste plain text in. A Markdown (`.md`) file is the better default, and here is where to keep it.

**Keep your skills as `.md` files in Google Drive, then link them into the Project.** This gives you one source of truth: when a process changes, you update the file in Drive once and every employee linked to it is current — no forked copies drifting apart. It also makes your skills instantly shareable. Hand a new hire or a teammate the Drive folder and they have the exact same trained employee you do. Skills you build for yourself become skills your whole team can run.

### One-Time Setup: Turn On Skill-Building in Every Chat

Do this once. It tells Claude to help you build and maintain skills in every conversation, not only inside a Project.

1. Go to claude.ai and click your profile icon in the top right.
2. Click **Settings**, then **Profile**.
3. Find the box that asks what personal preferences Claude should consider in its responses. Paste the text below into it and save.

```
Build and improve my skills as we work. My skills are reusable workflow files (.md or .txt) that live in my Claude Projects — each Project is one AI employee, and its skills are how that employee is trained. Whenever a repeatable process, a correction I had to apply, or a new learning comes up, proactively tell me — without waiting to be asked — whether it should be a new skill or an update to an existing one, and name which skill.

When creating or updating a skill, always:
1. Name + trigger: a clear name and a one-line "when to use this."
2. New vs. update: state whether it's a new skill or an update to a specific named skill.
3. Structure: Purpose / When to use, then Steps, then Gotchas & learnings, then Output format.
4. Changelog: note the date and what changed at the top.
5. Confirm first: show me the draft and get my sign-off before finalizing.
6. One canonical copy: keep a single source of truth (I keep mine as .md files in Google Drive) and tell me exactly where it lives so versions don't fork.

Keep skills concise and copy-paste ready. Fold in real learnings from our sessions, not generic advice.
```

From now on, whenever you and Claude land on a process worth keeping, Claude flags it and offers to turn it into a skill in this format. That is how your employees get smarter over time.

---

## Step 1: Complete the Prework (Do This Before the Workshop)

The prework has two jobs: connecting Google Drive to Claude and capturing your voice.

**To start:**

1. Go to claude.ai and start a new conversation.
2. Upload the file called `ai-agent-prework/SKILL.md` from this folder using the paperclip icon.
3. Type: "Start the prework."
4. Claude will guide you through the rest. Follow every step it gives you.

Do not move to Step 2 until Claude confirms both tasks are complete.

---

## Step 2: Run the Workshop

Once prework is done, you are ready to build your AI employee. The workshop opens with a short setup step (about 15 minutes) where you confirm your prework and install the scheduling tool you will use for any recurring work. Then it moves into the four phases.

**To start:**

1. Go to claude.ai and start a new conversation.
2. Upload the file called `ai-agent-workshop/SKILL.md` from this folder using the paperclip icon.
3. Type: "Start the workshop."
4. Claude will guide you through building your AI employee step by step.

The workshop covers four phases:

- **Phase 1:** Define who your AI employee is and what they own
- **Phase 2:** Connect the tools they need to do their job
- **Phase 3:** Build and test the skills that teach them your processes. You will see the real output first and refine it until you are happy. Only then does Claude write the final skill file. If a task repeats on a schedule, this is where you set up how it runs.
- **Phase 4:** Set them up in shadow mode so you can review their work before anything goes out

The only thing you need to bring is a clear answer to this question: if you could hire one person tomorrow to take something completely off your plate, what role would that be?

---

## Step 3: Shadow Mode (After the Workshop)

For the first seven days, your AI employee shows you their work before anything goes out. You review and approve. You do not do the work yourself.

Every time you send a correction, add it to the Project Instructions as a permanent rule. If it happened once, it will happen again. Making it a rule prevents that.

After seven days of consistent, accurate output, your employee operates with minimal oversight.

If your employee has recurring work, keep triggering those runs yourself during shadow mode so you see the first several before they run on their own. Once a task is proven, let the schedule you set up in Phase 3 take over. Remember that Claude Cowork scheduled tasks only run while your computer is awake and the Claude Desktop app is open.

---

## Questions

If you get stuck at any point during prework or the workshop, Claude will help you troubleshoot. Tell it exactly what you see on your screen and it will walk you through it.

For anything else or to hire me to build it for you, reach out at admin@agencyvilla.com.
