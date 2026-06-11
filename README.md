# Veritas

A job search intelligence tool built on the Anthropic Claude API. Evaluates roles against your background, scores them across four dimensions, and tracks your pipeline — so you spend time on the right opportunities.

**Live:** [itworkssly.github.io/veritas](https://itworkssly.github.io/veritas)

---

## What it does

Paste a job description and Veritas returns a structured evaluation:

- **Fit score** (0–100) across four dimensions
- **Domain Fit** — how closely the role maps to your actual experience
- **Growth Signal** — trajectory and scope expansion potential
- **Culture Signal** — JD language vs. your operating style
- **Comp & Logistics** — comp range, level, and work model against your parameters
- Strengths, gaps, and a plain-language verdict
- One-click add to pipeline tracker with stage, source, and notes

The tracker gives you a full view of everything in motion — applied, screening, interviewing, closed — with funnel analytics and a Vox briefing export for AI-assisted writing sessions.

---

## Demo mode

No API key? Hit the **▶ Demo** button to load a sample evaluation instantly. You'll see the full scoring interface, breakdown panel, and verdict with no setup required.

---

## Setup

1. Clone or download the repo
2. Open `index.html` in any browser — no build step, no dependencies
3. Enter your [Anthropic API key](https://console.anthropic.com/) in the key field
4. Optionally import your profile via `veritas_profile.json` for personalized scoring

Single-file app. Runs entirely in the browser.

---

## Profile

Veritas scores roles against a candidate profile — your background, comp floor, work model preferences, target companies, and deal breakers. Load yours via **Settings → Import Profile** or build it manually in the UI.

A sample profile schema is in `veritas_profile.json`.

---

## Stack

- Vanilla JS, HTML, CSS — no framework, no build tooling
- Anthropic Claude API for role evaluation
- `localStorage` for pipeline state
- Fully client-side

---

## Versioning

Current version: `v1.3.1`
Files follow underscore convention: the `VERSION` constant reads `veritas_v1_3_1`.

`index.html` is the live file served by GitHub Pages.

---

## The system

Veritas is one half of a two-tool job search system. The other half is **Vox** — a Claude Project configured as a persistent career strategy workspace. It handles cover letters, resume edits, interview prep, outreach drafts, and pipeline strategy, using context from your profile and Veritas briefings to produce work that sounds like a specific person, not a template.

The two tools share context through a structured briefing Veritas generates. You copy it, paste it at the start of a Vox session, and the writing workspace has full pipeline context immediately.

Both tools were designed by a PM. Claude handled implementation.

**[Vox documentation and setup guide →](./vox/README.md)**

---

## License

MIT
