# AGENTS.md

Guidance for an AI agent helping a user file a bug report in this repo.

## Purpose of this repo

This is the **public** intake point for technical bugs in SIPDUGA UI. It is
not for reporting a suspected violation (that goes through the SIPDUGA UI
app itself), and it is not a support/discussion forum. See `README.md` for
the human-facing explanation and the maintainer triage flow.

## Before filing an issue

1. **Never include confidential information** in the issue title, body, or
   any pasted screenshot/log — this repo and its issues are fully public.
   That means no report numbers, report passwords, names of
   reporters/witnesses/accused, chronology text, evidence contents, or
   anything else from an actual SIPDUGA report. If a user's bug report
   description contains any of this, ask them to remove it or redact it
   yourself before submitting, and say why.
2. Confirm the bug is about the *application* (broken page, form error,
   crash, wrong behavior) and not: a question about how to use the app, a
   request to check on a specific report's status, or a suspected violation
   itself. Redirect those elsewhere instead of filing an issue here.
3. Try to get enough detail to make the issue actionable: which page/flow
   (Buat Laporan / Ajukan Banding / Cek / home), what the user did, what
   they expected, what happened instead, and ideally the URL, device, and
   browser. Don't block on having every field — file with what's available
   and note what's missing.

## Filing the issue

Use the repo's issue form (`.github/ISSUE_TEMPLATE/bug_report.yml`) so the
report has the fields maintainers expect. If filing via `gh` CLI:

```bash
gh issue create \
  --repo sipduga/bug-reports \
  --title "<short, specific summary of the bug>" \
  --body "<filled-in form content, matching the template's fields>" \
  --label bug
```

Title guidance: describe the symptom and where it happens, e.g. "Ajukan
Banding: submit button stays disabled after uploading evidence" — not
generic titles like "Bug" or "Doesn't work".

## What NOT to do

- Don't file the same bug twice — search existing issues
  (`gh issue list --repo sipduga/bug-reports --search "<keywords>"`) first.
- Don't transfer issues into `sipduga/frontend` or `sipduga/backend`
  yourself even if you have access — that's a maintainer triage step (see
  `README.md`); your job here is filing a good report, not routing it.
- Don't close or edit other users' issues.
