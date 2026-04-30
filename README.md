# practice-incident

Static incident command center training page for a Webex website shortcut.

The page runs entirely in the browser by default. Buttons generate local workflow drafts for:

- Response thread
- Jira task
- Confluence notes
- Miro board update
- Approval email
- AI incident recap

Without an endpoint, each workflow button prepares a prefilled GitHub Issue trigger for the selected action. This keeps the Webex/GitHub Pages version useful without putting credentials in the browser.

External systems are modified only if the page is opened with an approved workflow endpoint:

```text
https://cooperinteractive.github.io/practice-incident/?endpoint=https://your-workflow-url
```

When an endpoint is configured, each button posts an `incident.workflow.action` JSON event. The endpoint can create or update Jira, Confluence, Outlook, Miro, or AI outputs and return links or revised draft text to the page.
