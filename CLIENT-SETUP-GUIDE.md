# How to Build Your First AI Employee
### A step-by-step guide. About 90 minutes. No code.

Read this once, then follow each step in order. You will end with an AI employee that owns one role in your business, runs on a schedule, and gets better every time you give it feedback.

---

## What You Need

- A free GitHub account (github.com). This is where your employee's instructions and skills live. Think of it as a Google Drive for your skills.
- Claude (Pro plan or higher) or ChatGPT (paid plan). Claude gives you the full hands-off setup. ChatGPT works with two manual steps, marked below.
- One role you would hire for tomorrow. Not a task. A role.

---

## How It Works

**One repo. One folder per employee.** Your repo is called `ai-employees`. Inside it, every employee gets a folder. Inside each folder go the skills that employee uses.

```
ai-employees/
  CLAUDE.md                      shared rules for every employee
  shared/context/                who you are and what your company does (built once)
  shared/voice-and-tone/         how you sound (built once)
  roles/
    legal-assistant/
      CLAUDE.md                  who they are, what they own, what they never do
      reference/                 your SOPs, samples, and what good looks like
      .claude/skills/
        morning-brief/SKILL.md   one job, step by step
        contract-review/SKILL.md
    content-writer/
      ...
```

You never create these files yourself. Your AI writes them and saves them to GitHub while you chat.

**Why GitHub?** Your skills live in one place and work with any AI. Switch from ChatGPT to Claude later and nothing moves. Hand a teammate the repo and they have the same trained employee.

**Prefer one repo per employee?** That works too. You get cleaner permissions and a separate history for each, and it is harder to manage. Start with one repo and split later if you need hard boundaries.

---

## Step 1: Make Your Repo (10 minutes)

1. Go to github.com and click **Sign up**. Skip this if you have an account.
2. Click the **+** in the top right, then **New repository**.
3. Name it `ai-employees`.
4. Choose **Private** unless you want the world to see your skills.
5. Check **Add a README file**.
6. Click **Create repository**.

---

## Step 2: Connect Your AI (10 minutes)

### Claude

1. Go to claude.ai/code and sign in.
2. Click the prompt to connect GitHub and approve it.
3. Install the Claude GitHub App on your `ai-employees` repo: github.com/apps/claude/installations/new. Private repos do not appear until you do this.
4. Back at claude.ai/code, pick `ai-employees` in the repository selector under the text box.

You can also use the Code tab in the Claude desktop app. You do not need a terminal.

### ChatGPT

1. In ChatGPT, open Settings and find Connectors (or Apps). Connect GitHub and pick your `ai-employees` repo.
2. Menus move. If you do not see these names, ask ChatGPT: "Where do I connect GitHub?"
3. Note: ChatGPT reads your repo well. Saving files into it is the part to check. If your ChatGPT cannot save, ask it to write each file, then paste it into GitHub yourself: open the repo, click **Add file**, then **Create new file**, type the path it gives you, paste, and click **Commit changes**.

---

## Step 3: Teach Your AI Who You Are (20 minutes)

Your employees start every job knowing nothing about you. Fix that once and they all know.

Open Claude or ChatGPT with your repo connected and drop in this link:

```
https://github.com/emmeliedelacruz/ai-employee
```

That is all you do. Your AI reads the repo, sees you have no context file yet, and starts.

Your AI will:

1. Ask for your website, bio, and anything that already describes your company. It reads them first, so you type less.
2. Ask the gaps: your role and goals, how you like updates, who your customers are, what you sell, your priorities this quarter, who is on the team, and the words only you would know.
3. Save it all to `shared/context/SKILL.md` and test that it can answer: who do I serve, what are my priorities, how do I like updates.
4. If your employee talks to people outside your team, capture your voice from three to five of your own messages and save it to `shared/voice-and-tone/SKILL.md`.

Write only what you would tell a new hire on day one. No passwords, no keys, no private client details. Keep the repo Private.

---

## Step 4: Build Your Employee in Chat (30 minutes)

Stay in the same chat. When your context file and voice skill are saved, your AI moves straight into building your first employee. If you come back later, drop the same link again. Your AI checks your repo and picks up where you left off.

If your AI cannot open links, download `README.md` from the repo and attach it to your chat.

Your AI will:

1. Ask who you would hire and what they own, what they decide alone, what needs your approval, and what they must never do.
2. Write the employee's folder and instructions.
3. Ask for your SOPs, sample outputs, and what good looks like, then save them.
4. Build the first skill by showing you real output. You react until it is right. Then it writes the skill.

Give it as much context as you can. Context is what makes the employee good.

**If a file lands on a branch called `claude/...` instead of `main`:** tell your AI "merge that into main." Skills only work for the routine once they are on main.

---

## Step 5: Create the Routine (10 minutes)

The routine wakes your employee up on a schedule and sends it to work. It runs in the cloud. Your computer can be off.

### Claude

1. Go to claude.ai/code/routines and click **New routine**.
2. **Name**: the employee, for example `Legal Assistant`.
3. **Prompt**: your AI writes this for you and tells you which box it goes in. It points at the folder. Example:
   ```
   You are the Legal Assistant. Read roles/legal-assistant/CLAUDE.md,
   then run the skills in roles/legal-assistant/.claude/skills/.
   Save anything you update to main.
   ```
4. **Repository**: `ai-employees`.
5. **Environment**: leave **Default**.
6. **Trigger**: pick Schedule. Choose a time a few minutes past the hour, like 8:07, because runs scheduled exactly on the hour can start late. The shortest allowed gap is one hour.
7. **Connectors**: Claude includes all of yours by default. Remove every one this employee does not need.
8. Click **Create**, then **Run now** to test.

Open the run to read what happened. A green status only means it started. It does not mean the job was right.

### ChatGPT

1. In ChatGPT, open **Scheduled** and create a task, or ask ChatGPT to create one for you.
2. Prompt: `Read the roles/legal-assistant folder in my ai-employees GitHub repo, then run its skills.`
3. Set the schedule (daily, weekly, or a custom time) and connect only the tools this employee needs.
4. Test the prompt in a normal chat first, then run the task once by hand.
5. Unattended tasks that write to other tools fail more often than manual runs. Keep your first employee read and draft only, and watch the first runs.

---

## Step 6: Train It for One Week

Your employee will make mistakes at first. Humans do too. Training is how it gets good.

1. **Review the output every day for at least a week** before you let it run on autopilot. People set up an AI, skip this step, and decide AI does not work.
2. **Give feedback in the same chat**, like you would to a person. Say what was wrong, how it should have been done, and what to do next time.
3. **Your AI updates the skill for you.** The next run uses the latest version. Do not fix the output by hand and move on. If you fix it by hand, the mistake comes back.
4. For feedback with a lot of detail, comment on the output in the Google Doc, then tell your AI to read the comments, fix them, and learn from them.
5. If you are not sure what to say, ask your AI: "What do you need from me to get this right?" AI is good at telling you how to train it.

---

## Step 7: Four Rules

1. **Review daily for a week.** Then let it run.
2. **Stagger your routines.** Do not run everything at 9 a.m. Spread them across the day. It saves usage and avoids busy times.
3. **Let AI write the skills.** AI is good at giving itself instructions. If you are unsure, chat with it and ask it to make the skill.
4. **Give each employee only what it needs.** Routines act as you. Give each one only the repo and the connectors it needs, so it does not take unnecessary actions or get confused.

---

## Step 8: Repeat

One employee at a time. Once the first one runs well for a week, add the next role or the next department. Each new employee is a new folder in the same repo.

---

## Optional: Skill-Building Setting

At the end of your build, your AI offers a one-time setting that makes it flag every new skill and update as you work. Say yes and it tells you exactly where to add it.

---

## If Something Goes Wrong

| What you see | Fix |
| --- | --- |
| Your repo does not appear in Claude | Install the Claude GitHub App on it: github.com/apps/claude/installations/new |
| Files went to a `claude/...` branch | Tell your AI to merge it into main |
| The routine ran but did the wrong thing | Open the run, read what happened, then give feedback in your build chat |
| The routine did nothing | Open the run. Check the repo is selected and the prompt names the right folder |
| A scheduled ChatGPT task did not save anything | Keep it read-only for now. Paste updates into GitHub by hand |

Claude and ChatGPT will help you troubleshoot. Tell it exactly what you see on screen.

For anything else, or to hire me to build it for you, reach out at admin@agencyvilla.com.
