# PM Skill Reference for Agencies and Service Providers

Read this file before building any skill that involves client work for an agency or service
provider. The PM skill is a foundational skill for these businesses. It allows the AI employee
to locate client files and context without the human having to point them to it every time.

---

## What the PM Skill Does

The PM skill teaches the AI employee how to find client information in whatever structure the
attendee currently uses. Because attendees have no standard structure, the skill is built around
their actual setup, not an ideal one. Work with what exists.

The employee should never ask the human "where is the file for [client]?" If that question would
ever come up, the PM skill is not working.

---

## How to Extract Their Current Structure

Because every attendee organizes differently, ask these questions to map what they actually have:

"Walk me through how you find a client's files right now. If I said the name of a client, what
would you do first to find their stuff?"

Then dig into the specifics:

- "Is everything in Google Drive, or is it split across Drive and other tools?"
- "Do clients each have their own folder, or is work organized by project type instead?"
- "What is usually in a client folder? Contracts, briefs, deliverables, notes, all of the above?"
- "Is there a master list anywhere of all your active clients? A spreadsheet, a CRM, a doc?"
- "Where do you keep notes from client calls or meetings?"
- "Where do you store the work in progress before it goes to the client?"

Map their answers into a structure diagram in plain language before writing the skill. Show it
to them and ask: "Is this accurate? Anything missing?" Fix it before building.

---

## PM Skill Structure

Build the skill using this format, filled in with their actual structure:

```
---
name: pm-client-locator
description: >
  Use this skill at the start of any task that involves a specific client. Use it to locate
  all relevant files, history, and context before beginning work. Always run this skill first
  when a client name is mentioned. Never ask the human to provide client files that can be
  found using this skill.
---

# PM Client Locator

## What This Skill Does

This skill tells you exactly where to find everything you need for any client before you start
working on their account. Run this skill first. Do not ask the human for files.

## How Client Files Are Organized

[Describe their actual structure in plain language. Example: "Each client has a folder in Google
Drive named with their company name. Inside each folder there are four subfolders: Contracts,
Active Projects, Deliverables, and Notes. The master client list is in a Google Sheet named
Client Roster in the Agency Operations folder."]

## How to Find a Client

When a client name is given, do the following in order:

1. [First step based on their actual structure. Example: "Open the Client Roster sheet and
   confirm the client is listed as active."]
2. [Second step. Example: "Navigate to the client's named folder in Google Drive."]
3. [Third step. Example: "Open the Notes subfolder and read the most recent call notes before
   doing anything else."]
4. [Continue for all steps needed to locate and orient to a client's work.]

## What to Pull Before Starting Any Client Task

Before beginning any deliverable for a client, confirm you have read:
- [Document type 1 and where it lives]
- [Document type 2 and where it lives]
- [Add all that apply]

If any of these documents are missing from the client folder, flag it to the human before
proceeding. Do not guess at missing information.

## If the Client Is Not in the System

If a client name is given and they do not appear in the roster or do not have a folder:
1. Flag this to the human immediately.
2. Do not create folders or records on your own.
3. Ask the human to confirm the client name or set up the folder before proceeding.

## Notes on Irregular Structures

[If their structure is inconsistent or has known exceptions, document them here. Example:
"Clients onboarded before 2023 may have files in the Old Clients archive folder instead of
the main Drive. Check there if the client folder is not found in the primary location."]
```

---

## Connecting Their Tools to Claude

If their files live outside Google Drive, read references/integrations.md and walk them through
connecting the right tool before building the PM skill. The skill only works if Claude can
actually access the files.

If their structure is split across multiple tools with no single source of truth, help them
consolidate before building the skill. Say: "Before your AI employee can find client files
reliably, we need one place where everything lives or at least a map that points to each
location. Let's spend five minutes deciding where that master index should live and I will
help you set it up."

---

## Testing the PM Skill

After building it, test with a real client:

"Give me the name of a current active client. Let's see if your employee can find everything
they need without you pointing to anything."

Run the skill. Check whether the employee:
- Located the correct client folder
- Pulled the right documents before starting
- Did not ask the human for anything it should have found itself

If it asks the human for information that should be in Drive, the skill has a gap. Identify
which step failed, update the skill, and save the new version over the file in the master skills
folder before moving on.
