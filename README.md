# Orebridge — local mining marketplace MVP

A no-dependency, local-first workflow demo. Orebridge is a temporary working name. All seed companies, projects, financial amounts and documents are fictional.

## Start

Requires Node.js 22 or newer. From this directory:

```sh
node server.mjs
```

Open http://127.0.0.1:4173 in your browser. The server only listens on your own computer. Stop it with Ctrl+C. No cloud accounts, package installation or hosting subscription are required. Existing computer, electricity and any coding-assistant subscription/usage are separate.

## Try the complete journey

1. Start as Investor. Open Saryarka Copper and request access.
2. Switch to Project owner using the sidebar selector.
3. Open Access requests and approve the request.
4. Switch back to Investor, open Deal rooms, and read the fictional project notes.
5. Post a question, switch to Project owner and respond.
6. Revoke access as the owner; the investor can no longer use that deal room through the interface.
7. Add a fictional project as Project owner. Adjust investor preferences and try the filters.

Data is stored in this browser's localStorage for this exact origin. It persists across reloads but is not shared with another computer, browser or port. Browser storage may be cleared. Export demo data periodically; the export is a JSON snapshot, with no import interface yet. To reset, clear this site's browser storage. Role selection resets to Investor after reload.

## What works

- Fictional project directory, search, metal/stage filters and saved opportunities.
- Investor preferences with explainable deterministic matching.
- Creation of project/opportunity records with validation.
- Access request, approval, decline and revocation workflow.
- Deal-room text notes and questions/answers.
- Local persistence and JSON export.
- Responsive interface and keyboard-accessible native forms/dialogs.

## Important boundary

This is a functional workflow prototype, not a production multiuser platform. The role switch is for demonstration, not authentication. All demo data exists in browser storage and can be inspected or changed by the person using that browser. UI access checks are not a security boundary. Do not enter real personal data, confidential reports, credentials or actual investment offers.

There are no real accounts, backend database, cross-device collaboration, signed NDAs, file uploads, identity checks, email delivery, tamper-resistant audit records or production recovery controls. Do not publicly deploy this as a secure investment service.

## Next build phase

Preserve the validated workflows and add a server-side API and database, real organization membership and session authentication, server-enforced deal-room authorization, private uploads with scanning, and audit records. Reassess the agreed Next.js/NestJS/PostgreSQL stack at that point. The current dependency-free frontend is deliberately a fast prototype rather than a completed implementation of that architecture.

Before a real-user pilot, verify hosting residency, data handling and the business's regulatory model; test access isolation and recovery; then obtain a supplier quote. No hosting or paid service has been purchased for this demo.

## Checks

```sh
node --test domain.test.mjs
```

Tests cover the request/approval/revocation journey, duplicate requests, invalid decisions, project validation, matching and JSON persistence. Browser visual testing should be repeated before sharing; the automated browser available during creation could not initialize.

An optional read-only WebMCP tool lists fictional opportunities when supported by the browser. Its registration could not be validated in a supported browser during creation. It is not required to use the app.
