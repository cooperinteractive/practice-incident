# practice-incident

Static Webex incident space builder and response field guide for the Practice Incident simulation.

The page is designed to live as a Webex website/content tab while staying safe as a public static site. It does not contain platform credentials, API keys, webhook secrets, private emails, real incident facts, or automatic writes to external systems.

The current experience generates a Webex-native operating model from one editable intake:

- simulation-labeled incident packet
- dedicated Webex space plan
- command-post card preview
- phase thread starters
- responder membership plan
- Jira, notes, tracker, and Outlook handoff plan
- AI closeout recap draft
- downloadable JSON packet
- copyable Webex Adaptive Card JSON

The companion field guide at `response-guide.html` is an original interactive rewrite of a supplied incident-response cheat-sheet concept. It keeps the value but drops the poster clutter: five phases, decision prompts, role cards, presenter mode, copyable outputs, markdown download, and print/save PDF. It does not include source-sheet branding, contact details, phone numbers, addresses, slogans, or copied layout.

Button behavior is intentionally local until an organization-approved Webex bot, Webex MCP workflow, or internal Webex API service is selected. The buttons update the visual room preview, timeline, activity log, and active artifact so the client can understand exactly what the eventual automation will create.

Recommended live architecture:

1. Keep this page as the visual command tab or translate it into a native Webex App Hub surface.
2. Let an approved Webex bot/MCP/API service own writes to Webex rooms, memberships, messages, cards, and webhooks.
3. Keep all credentials server-side in the approved environment.
4. Return non-secret status and artifact links to the page after each approved action.
5. Preserve the simulation label on every generated artifact until the exercise is formally promoted.

Current live page:

```text
https://cooperinteractive.github.io/practice-incident/
https://cooperinteractive.github.io/practice-incident/response-guide.html
```
