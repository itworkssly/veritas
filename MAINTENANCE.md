# Veritas Maintenance Pass

A repeatable checklist for keeping Veritas clean. Run a pass after a stretch of feature work, or whenever something behaves oddly. Cadence is activity-driven, not calendar-driven. A 147KB single-file app does not accumulate much rot, so do not over-schedule.

To run a pass, open a session in the Vox project and say "run the Veritas maintenance pass." Work through the steps below in order.

## 1. Pull live

Pull `index.html` from the repo before touching anything. Never refactor against a local copy. Capture the SHA for the eventual push.

## 2. Scan for drift

Look for logic that should be shared but has been copy-pasted into multiple call sites. The closed-detection condition (`isClosed`) is the canonical example. If a check appears inline in more than one place, it belongs in a helper.

Grep for repeated literals. Common culprits:

- Closed-detection (`status==='closed'`, terminal stage lists)
- Stage allowlists (note: the active-stage allowlist intentionally excludes `evaluated`, so it is NOT the complement of `isClosed`. Do not merge them.)
- Stage label maps
- Date math

## 3. Dedupe

Extract repeated logic into a single top-level helper. Replace every inline copy with a call to it. Remove any local helpers that now shadow the global with an identical definition.

## 4. Test before push

- Extract the script block and run it through a JS parser to confirm clean syntax.
- For any logic change, write a short table of input shapes with expected outputs and run it. Always include the edge cases: a status-closed record with an active stage, and an `evaluated` record.

## 5. Bump version

Patch releases (bugfix, refactor) increment the third number. Update all three spots:

- `<title>` tag
- `VERITAS_VERSION` constant (underscore convention: `veritas_v1_3_2`)
- "What's new" banner copy, written to the style guide

## 6. Push and reconcile README

- Push `index.html` with a descriptive commit message.
- Update the README version line and the `VERSION` constant reference to match.
- Push the README.

## Style note

All user-facing copy (banner text, commit messages where they surface) follows the Vox style guide. No em dashes, no AI vocabulary, no rule-of-three, no puffery, active voice.
