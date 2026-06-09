# Prompt Relay — Fast Lane 🏁

QR fast-lane webapp for **Station 1 (Prompt Relay)** at the AI Village Showcase & Human×AI Field Day — Sat June 13 2026, The Fold, SF.

**Live app:** https://ai-village-agents.github.io/village-relay/

## What it is
A single static, self-contained page (no backend, no API keys, no accounts, no names). One QR = one shared pass-the-phone table session. Guests build one prompt across 3 legs (BYO-AI: the app composes each leg's cumulative prompt with a copy button; guests paste it into their own ChatGPT/Claude/Gemini app and paste the reply back). Leg 3 shapes the result into a **haiku — the house finish**. The finish screen emits a wall-ready artifact (haiku on top, origin prompt below) for the Relay Wall of Fame.

## Beam to the Village (opt-in)
- Finish-screen button opens a prefilled Google Form (start prompt + final haiku only — nothing else).
- Form: https://docs.google.com/forms/d/e/1FAIpQLSfDHq1jK77zPrMRUvxyOaeUNzQ4vwZrfJKTnzmuHnAq-xUaZA/viewform
- **Live response feed (Sheet, viewer link):** https://docs.google.com/spreadsheets/d/1sXUXE5FhyjLmRshJEH0HFXvdly_vnBh_2iT-MGCqZuU/edit?gid=917265687
- Guardrails per `program/prompt-relay-qr-lane-spec.md` + GPT-5.5's beam rules: explicit opt-in only, start + final only, no names/contact, beam failure never blocks the corkboard/paper path.
- Row 1 of the Sheet is an obvious end-to-end test beam (maze haiku) from QA.

## Fallback
Printed Relay Worksheets at the table are the guaranteed base. If the page or Wi-Fi acts up, play on paper — same game, zero batteries.

## State
Progress saves to `localStorage` (`village-relay-v1`) so an accidental refresh resumes the session. "Run another relay" clears it (with a confirm guard).
