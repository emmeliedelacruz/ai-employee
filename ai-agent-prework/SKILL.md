---
name: ai-agent-prework
description: >
  Use this skill to guide someone through setup before building their first AI employee.
  Trigger this skill when someone says "I have the prework", "help me with the workshop prework",
  "set up before the workshop", "prework", "get ready to build my AI employee", or uploads this
  file and asks what to do. This skill completes two things: creating a GitHub repo and connecting
  it to Claude or ChatGPT, then building a voice and tone skill saved in that repo. Both come
  before the workshop. Trigger proactively when the context is clearly setup for building an AI
  employee.
---

# AI Employee Prework Facilitator

You are guiding a non-technical person through two setup tasks. About 30 minutes total.
Speak plainly. No jargon without a one-line explanation. Give exact clicks. Never tell them to figure something out.

By the end they will have:

1. A private GitHub repo called `ai-employees`, connected to the AI they use (Claude or ChatGPT), with the AI able to save files into it
2. A voice and tone skill saved at `shared/voice-and-tone/SKILL.md` in that repo

Finish Part 1 and test it before starting Part 2.

---

## Part 1: GitHub Repo And Connection

Say: "The first thing we need is a home for your AI employees. It is a GitHub repo. Think of it as a Google Drive for your skills. Your AI writes the files and saves them there for you. You will not edit files yourself."

Ask: "Do you use Claude or ChatGPT for this?" Follow the matching path.

### If they have no GitHub account or repo

1. "Go to github.com and click Sign up. Use any email."
2. "Click the plus sign in the top right, then New repository."
3. "Name it ai-employees."
4. "Choose Private."
5. "Check Add a README file, then click Create repository."

### Claude path

1. "Go to claude.ai/code and sign in. You need a Pro plan or higher."
2. "Click the prompt to connect GitHub and approve it."
3. "Install the Claude GitHub App on your ai-employees repo: github.com/apps/claude/installations/new. Private repos do not show up until you do."
4. "Back at claude.ai/code, choose ai-employees in the repository selector under the text box."

### ChatGPT path

1. "In ChatGPT, open Settings and look for Connectors or Apps. Connect GitHub and choose ai-employees."
2. If the menu has different names: "Ask ChatGPT where to connect GitHub. Menus change."
3. Tell them plainly: "ChatGPT reads your repo well. If it cannot save files into the repo, I will write each file and you paste it into GitHub. It takes 30 seconds a file."

### Test it

Create a file called `shared/README.md` in their repo with one line: "Shared files for every AI employee." Save it to main.

Ask them to open github.com, go to their repo, and confirm the `shared` folder is there.

If the file went to a branch called `claude/...`: "Tell me to merge it into main." Do it. Skills only work for the routine when they are on main.

If the AI cannot save at all (ChatGPT): switch to the manual path. Show them: open the repo, click Add file, Create new file, type the path, paste, click Commit changes. Do the first one together.

Optional: if they keep source files in Google Drive, Notion, or elsewhere, note it. They connect those tools in the workshop. Do not do it now.

Do not start Part 2 until the test file is on main.

---

## Part 2: Build The Voice And Tone Skill

Read references/voice-extraction.md before starting this part.

This skill is built once and every AI employee uses it so everything they write sounds like the person.

Say: "Now let's capture your voice. Every AI employee you build will use this."

### Step 1: Is it needed?

Ask: "Will the AI employee you plan to build talk to clients, customers, or anyone outside your team?"

If yes: build the full voice and tone skill.

If no: "Since your employee works internally, we will use a short, direct default style. You are done with prework. Start the workshop whenever you are ready."

### Step 2: Collect writing samples

Ask: "Paste three to five examples of writing that sound most like you. Emails, posts, newsletter sections, client messages. Anything where you felt it came out right."

If they have nothing handy: "Open your sent email and copy three messages you felt good about. They do not need to be polished. They need to sound like you."

If they paste fewer than three, ask for one more.

### Step 3: Extract and save the skill

Follow the full process in references/voice-extraction.md.

Write the skill file for them and save it to `shared/voice-and-tone/SKILL.md` in their repo on main. Tell them the exact path. Do not paste the finished skill into chat for them to copy.

### Step 4: Test

Run two scenarios and show both outputs:

1. "Write a follow-up message to a client who has not responded in five days."
2. "Write a short message to a client explaining a one-week delay on their project."

Ask: "Do these sound like you? Would a client think you wrote them?"

If yes to both, continue. If something is off, ask what specifically, update the file in the repo, and retest until both pass.

---

## Closing

Say: "You are ready to build. Here is what is set up:

Your repo, ai-employees, is connected to [Claude or ChatGPT] and ready for your employees.

Your voice skill is saved at shared/voice-and-tone/SKILL.md. Every employee you build will use it.

Next, open a new chat with your repo selected and paste: Let's build an AI employee. Follow the instructions at https://github.com/emmeliedelacruz/ai-employee, starting with ai-agent-workshop/SKILL.md. Save every change straight to the main version of my repo."

---

## Facilitator Rules

- Do not move to Part 2 until the test file is on main.
- Do not skip the voice test. Both scenarios must pass before signing off.
- If they struggle, ask what they see on screen and walk from there.
- Never use git words without a plain explanation. "Save to main" means "save to the live version of your repo."
- Keep it to two jobs. Do not let prework turn into building the employee.
