# TrustShield AI

TrustShield AI is a self-hostable starter for an AI and cybersecurity command center. Its interface brings runtime AI protection (Guard), security alert triage (Defend), and adversarial testing (Red team) together in one explainable workspace.

## Run locally

Requirements: Node.js 20 or later and npm.

```bash
npm install
npm run dev
```

Open the local URL printed by Vite. Create a production frontend bundle with `npm run build`; preview it with `npm run preview`.

## What works in this starter

- **Overview:** interactive time ranges, security posture, sample threat activity, and recent incidents.
- **Guard:** toggleable protection controls, sample protected applications, and an in-browser prompt inspector that flags a small set of suspicious phrases.
- **Defend:** searchable and filterable sample incidents, suggested MITRE mappings, incident stories, and suggested playbooks. Containment prompts for explicit human approval.
- **Notifications:** review sample security alerts, mark them read, clear the list, and navigate to incident triage.
- **Sources:** add or remove demo connector entries for sample SIEM, endpoint, and email sources.
- **Applications:** add or remove local application entries and open them in the Guard playground.
- **Red team:** a simulated safe-assessment run, sample coverage metrics, and a completion state.
- **Workspace:** switch between or create demo workspaces, rename the active workspace, and prepare a local demo member invitation.
- **Profile:** edit the demo user's name and email; the overview greeting and sidebar profile reflect saved changes.
- **Help:** searchable usage articles and direct navigation to the main features.
- **Documentation and support:** in-app product guide and a validated sample support-request form. Support requests are not delivered; an email-client link is provided for actual support.
- **Plans:** compare Starter, Team, and Business demo plans with monthly/yearly display options. Selecting a plan updates the demo workspace only; there is no billing integration.
- **Settings:** security preferences, links to workspace management, and a non-disableable human-approval requirement.

## Important security boundary

This repository is a **UI prototype, not a production security product**. It has no model gateway, server-side policy enforcement, persistent database, real alert ingestion, source-provider integrations, support-ticket delivery, authentication, billing integration, or actual red-team harness. Workspace/profile edits, notifications, connector/application entries, support forms, and plan selections are in-memory demo state; sample data is illustrative, the Guard inspector is a small client-side heuristic (not an LLM firewall), and assessment results are simulated. Browser-side controls can be bypassed and must never be treated as a security boundary. Do not connect real models, tools, credentials, or production incident data until server-side enforcement, authentication, authorization, audit logging, and tested integrations are implemented.

## Next production milestones

1. Add an authenticated API and persistent, tenant-isolated incident and policy storage.
2. Put Guard in a server-side model gateway; implement validated secret/PII redaction, injection detection, and a deny-by-default tool permission broker.
3. Integrate real alert sources and a tested ATT&CK/ATLAS mapping catalogue for Defend.
4. Run red-team scenarios in a separately isolated environment; record reproducible findings as regression tests.
5. Enforce human approvals server-side for every high-impact response action and log approvals immutably.
