# practice-incident

Static incident command center training page for a Webex website shortcut.

The page runs in the browser and now includes a simulation artifact pack for:

- ClickUp task tracker
- Jira validation issue
- Notes draft
- Miro board brief
- Approval email
- AI incident recap

The deployed demo uses no external workflow endpoint by default. Workflow cards update the in-page draft preview and expose contextual links. ClickUp, Jira, and notes links point to simulation proof artifacts created through the connected tools. Miro board brief and AI recap stay in the page by default because embedded browser sessions may block some platform pages. Outlook opens a compose screen using the current intake values and does not send.

When an approved endpoint is configured, workflow buttons post the current simulation intake to that server-side bridge. If the bridge returns real artifact URLs, the launch buttons update from static examples to those returned links, such as `Open ClickUp Task` or `Open Jira Issue`. The page still stores no platform credentials.

Submit Intake now creates a functional local simulation packet:

- required-field validation
- saved local intake record
- exact submitted and next-update timestamps
- copyable intake packet
- downloadable JSON
- saved submission history with reload

This keeps the Webex/GitHub Pages version useful without putting credentials in the browser or relying on long encoded trigger URLs.

External systems are modified only if the page is opened with an explicitly approved workflow endpoint:

```text
https://cooperinteractive.github.io/practice-incident/?endpoint=https://your-workflow-url
```

When an endpoint is configured, each button posts an `incident.workflow.action` JSON event. The endpoint can create or update ClickUp, Jira, notes records, Outlook, Miro, or AI outputs and return links or revised draft text to the page.

Use the local endpoint starter in `../WorkflowEndpoint` for safe bridge testing only. It keeps external writes disabled by default and requires server-only environment variables before any platform adapter can write. Do not set a hosted endpoint as the default unless the endpoint host has been explicitly approved.

Current live page:

```text
https://cooperinteractive.github.io/practice-incident/
```
