# practice-incident

Static incident command center training page for a Webex website shortcut.

The page runs in the browser and now includes a simulation artifact pack for:

- ClickUp task tracker
- Jira validation issue
- Notes draft
- Miro board brief
- Approval email
- AI incident recap

Without an endpoint, workflow cards update the in-page draft preview and expose contextual links. ClickUp and Jira links are labeled as static examples so the user does not mistake them for records that are rewritten by the browser. Notes, Miro board brief, and AI recap stay in the page by default because embedded browser sessions may block some platform pages. Outlook opens a compose screen using the current intake values and does not send.

Submit Intake now creates a functional local simulation packet:

- required-field validation
- saved local intake record
- exact submitted and next-update timestamps
- copyable intake packet
- downloadable JSON
- saved submission history with reload

This keeps the Webex/GitHub Pages version useful without putting credentials in the browser or relying on long encoded trigger URLs.

External systems are modified only if the page is opened with an approved workflow endpoint:

```text
https://cooperinteractive.github.io/practice-incident/?endpoint=https://your-workflow-url
```

When an endpoint is configured, each button posts an `incident.workflow.action` JSON event. The endpoint can create or update ClickUp, Jira, notes records, Outlook, Miro, or AI outputs and return links or revised draft text to the page.

Current live page:

```text
https://cooperinteractive.github.io/practice-incident/
```
