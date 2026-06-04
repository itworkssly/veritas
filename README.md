# Veritas

**The truth about every role. The voice to pursue it.**

Veritas is an AI-native job search intelligence system built on the Claude API. It evaluates roles, scores fit across four dimensions, and tracks your pipeline from first look to final round.

---

## What it does

**Evaluate** — Paste a job description. Veritas scores fit across Domain, Growth, Culture, and Comp signals, surfaces your strengths and gaps against the role, and gives you a clear recommendation before you invest time in the process.

**Track** — Every role you've touched, organized by stage. Applied, screening, HM screen, interview, final round, offer, closed. The full picture in one view.

**Dashboard** — Funnel analytics across your pipeline. Where are you converting? Where are you losing? What's stale?

**Vox** — One-click briefing export to your AI writing workspace. Vox handles cover letters, interview prep, follow-up strategy, and positioning. Veritas feeds it the context.

---

## How it works

Veritas runs entirely in the browser. No backend, no database, no accounts. Your data lives in localStorage. Your API key never leaves your machine.

Built as a single HTML file. Deployable anywhere.

---

## Stack

- Anthropic Claude API (claude-sonnet-4-20250514)
- Vanilla JS, no framework
- Local storage for persistence
- Designed and spec'd in plain language. Engineered with Claude.

---

## The system

Veritas is one half of a two-tool job search system.

| Tool | Role |
|------|------|
| **Veritas** | Evaluation, scoring, pipeline tracking |
| **Vox** | Writing, prep, strategy, positioning |

The two tools share context through a structured briefing Veritas generates. Vox reads it at the start of every session. You stay oriented. Every conversation starts informed.

---

## Background

Built by a PM with 15 years in TA and People Operations who needed a better way to run a serious job search. The scoring model, dimensions, UX, and briefing format were all designed by hand. Claude handled the implementation.

This is what AI-native product development looks like in practice: a real problem, a clear spec, a working tool.

---

*Veritas. From the Latin for truth.*
