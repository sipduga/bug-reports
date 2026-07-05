# SIPDUGA UI — Bug Reports

Public bug-tracker for the SIPDUGA UI application. Use this repo to report
**technical problems** with the app (broken pages, form errors, things that
don't work as expected).

This is not where you report a suspected violation — use the SIPDUGA UI app
itself for that.

## Reporting a bug

Open a new issue and fill in the "Bug report" form. Please **do not include
any confidential report details** (report numbers, names, chronology,
evidence, etc.) — this repository and its issues are public.

## For maintainers: triage flow

The application code lives in two private repos (`sipduga/frontend`,
`sipduga/backend`), which external reporters don't have access to. This repo
exists so anyone can file a bug without needing access to those repos.

When triaging an incoming issue here:

1. Confirm it's a real, reproducible bug (not a support question or a
   suspected-violation report that landed here by mistake).
2. Decide which repo it belongs to (`frontend` or `backend`).
3. Use GitHub's **Transfer issue** feature (issue sidebar → "Transfer issue")
   to move it into the right private repo — this preserves the original
   report text and requires write access to both repos, which reporters
   don't have, so it's safe to do without exposing anything.
4. Close/label the original if the transfer doesn't automatically close it,
   and continue all engineering discussion in the private repo from then on.
