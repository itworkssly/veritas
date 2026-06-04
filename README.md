# Veritas

A job search intelligence tool built on the Anthropic Claude API. Evaluates roles against your background, scores them across four dimensions, and tracks your pipeline — so you spend time on the right opportunities.

**Live:** [itworkssly.github.io/veritas](https://itworkssly.github.io/veritas)

---

## What it does

Paste a job description and Veritas returns a structured evaluation:

- **Fit score** (0–100) broken down across four dimensions
- **Domain Fit** — how closely the role maps to your actual experience
- **Growth Signal** — trajectory and scope expansion potential
- **Culture Signal** — JD language vs. your operating style
- **Comp & Logistics** — comp range, level, work model against your parameters
- Strengths, gaps, and a plain-language verdict
- One-click add to pipeline tracker with stage, source, and notes

The tracker gives you a full view of everything in motion — applied, screening, interviewing, closed — with funnel analytics and a Vox sync log for AI-assisted career content.

---

## Demo mode

No API key? No problem. Hit the **▶ Demo** button next to Evaluate to load a sample role evaluation instantly. You'll see the full scoring interface, breakdown panel, and verdict with no setup required.

---

## Setup

1. Clone or download the repo
2. Open `veritas_v1_2_public.html` in any browser — no build step, no dependencies
3. Enter your [Anthropic API key](https://console.anthropic.com/) in the key field
4. Optionally import your profile via `veritas_profile.json` for personalized scoring

That's it. Single-file app, runs entirely in the browser.

---

## Profile

Veritas scores roles against a candidate profile — your background, comp floor, work model preferences, target companies, and deal breakers. Load yours via **Settings → Import Profile** or build it manually in the UI.

A sample profile schema is available in `veritas_profile.json`.

---

## Stack

- Vanilla JS, HTML, CSS — no framework, no build tooling
- Anthropic Claude API (`claude-sonnet-4-20250514`) for role evaluation
- `localStorage` for pipeline state
- Runs fully client-side

---

## Versioning

Current version: `v1.2`  
Files follow underscore convention: `veritas_v1_2_public.html`

---

## Background

Veritas started as a personal tool during a job search and grew into a proof of concept for AI-native workflow design. The scoring model, dimension weights, evaluation prompt, and UX were designed by a PM; Claude handled implementation. The companion workspace for career content (cover letters, interview prep, outreach) is Vox, a Claude Project.

---

## License

MIT
