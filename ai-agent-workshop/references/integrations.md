# Integrations Reference

Read this file when a tool connection is needed. The goal is simple: connect only the tools this
specific employee's workflow needs, using the easiest method available. Start with the Connectors
directory. Fall back to Zapier or Make only for tools the directory does not cover.

Do not tell the attendee to figure anything out. Give exact steps from wherever they are.

---

## Connect Based on the Workflow, Not a Checklist

Every employee needs a different set of tools. A reporting employee needs different connections
than an inbox employee or a client-onboarding employee. Do not connect everything. Look at where
this employee's work comes in and where its finished outputs need to go, and connect only those
tools.

Ask: "For this employee to do its job end to end, where does its work come from and where do its
outputs need to land?" Connect the tools that answer that question. Nothing more.

---

## Start With the Connectors Directory

Claude connects to a large and constantly growing set of tools directly, with no third-party
bridge. This is always the first thing to check. Do not assume a tool is missing.

Steps:

1. "Go to claude.ai and click your profile icon in the top right."
2. "Click Settings, then Connectors."
3. "Search for the tool by name."
4. "If it is listed, click Connect, sign in, and authorize the access it asks for."
5. "Come back here and confirm it is connected."

Google Drive is connected during prework. Connect the rest here as each one comes up in the
build. If a tool is in the directory, this is the whole job. Move on.

---

## When a Tool Is Not in the Directory: Zapier or Make

Use this path only for a tool that is not in the Connectors directory. Zapier and Make are no-code
bridges. Treat the attendee as non-technical and give exact steps.

### When to use Zapier vs Make

Use Zapier if the attendee has never used either. It is simpler and has more pre-built templates.
Use Make if they already have a Make account or if their workflow is complex with multiple
branches.

### The pattern

Whatever the tool, the shape is the same. Something happens in the tool (a new form submission,
a new CRM record, a new row). The bridge sends that information to Claude. Claude processes it and
responds. The bridge routes the response wherever it needs to go (a Slack message, an email draft,
a CRM note, a new row). Build every fallback connection around that pattern.

### A note on the model in the API call

The Zapier and Make paths call the Claude API, which requires a model ID in the request. Model
names change over time. Do not hardcode an old one. Get the current model ID from Anthropic's
docs at docs.claude.com and paste it in where the payload below shows REPLACE_WITH_CURRENT_MODEL_ID.

---

## Setting Up a Zapier Connection to Claude

1. "Go to zapier.com and create a free account if you do not have one."

2. "Click Create Zap."

3. "For the Trigger, search for [their tool name]. Select the event that should start the
   workflow. For example: New Form Submission, New Row in Spreadsheet, New Lead in CRM."

4. "Connect your [tool name] account when prompted and select the specific form, sheet, or
   pipeline you want to monitor."

5. "Click Continue and test the trigger to confirm Zapier can read data from your tool."

6. "For the Action, search for Webhooks by Zapier. Select POST."

7. "In the URL field, enter: https://api.anthropic.com/v1/messages"

8. "Set Payload Type to JSON."

9. "In the Data section, enter this exactly, replacing the model ID with the current one from
   docs.claude.com and replacing the prompt text with what you want Claude to do:"

```json
{
  "model": "REPLACE_WITH_CURRENT_MODEL_ID",
  "max_tokens": 1024,
  "messages": [
    {
      "role": "user",
      "content": "Here is the incoming information: {{your trigger data field}}. [Describe what Claude should do with it and what format the output should be in.]"
    }
  ]
}
```

10. "In the Headers section, add:"
    - Key: x-api-key | Value: [their Anthropic API key]
    - Key: anthropic-version | Value: 2023-06-01
    - Key: content-type | Value: application/json

11. "To get an Anthropic API key: go to console.anthropic.com, sign in or create an account,
    click API Keys, and create a new key. Copy it and paste it into the Zapier header."

12. "Test the action. You should see a response from Claude in the test output."

13. "Add a final action to send Claude's response to wherever it needs to go: a Slack message,
    a Gmail draft, a CRM note, a new spreadsheet row, or wherever makes sense."

14. "Name the Zap clearly, for example: New Client Inquiry to Claude to Gmail Draft. Turn it on."

---

## Setting Up a Make Connection to Claude

Use this for attendees who already use Make or need more complex branching logic.

1. "Go to make.com and sign in or create an account."

2. "Click Create a new scenario."

3. "Add a module for [their tool]. Select the trigger event."

4. "Add an HTTP module. Select Make a request."

5. "Configure the HTTP module:"
   - URL: https://api.anthropic.com/v1/messages
   - Method: POST
   - Headers: Add x-api-key with their Anthropic API key, anthropic-version as 2023-06-01,
     content-type as application/json
   - Body type: Raw
   - Content type: JSON

6. "In the body, enter this, replacing the model ID with the current one from docs.claude.com:"

```json
{
  "model": "REPLACE_WITH_CURRENT_MODEL_ID",
  "max_tokens": 1024,
  "messages": [
    {
      "role": "user",
      "content": "{{your trigger data}}. [What Claude should do and what format to respond in.]"
    }
  ]
}
```

7. "Map the response to the next module in their workflow."

8. "Run the scenario once manually to test. Confirm Claude's response appears correctly."

9. "Turn the scenario on and set the schedule for how often it checks for new triggers."

---

## When Setup Fails

If the attendee gets stuck on a step, do not tell them to refer to documentation. Ask them to
describe exactly what they see on screen and walk them through it from that point. If an error
appears, ask them to read the error message out loud and diagnose from there.

If a tool is not in the directory and has no Zapier or Make connector either, ask: "Is there
another tool in your workflow that does connect and that feeds into or out of this one?" Find the
nearest connected point and bridge from there.
