---
name: log-defect
description: Write a structured defect / bug report from the standard template, enforcing mandatory fields. Use when the user wants to log, file, raise, write up, or report a bug or defect, or asks for the defect template.
---

# Log a defect

Turn what the user tells you about a bug into a complete report that follows
[templates/defect-template.md](templates/defect-template.md). Keep the template's
section order and field names exactly as they are, so every report looks the same.

## Mandatory fields

A report is not complete until all of these have real values (not placeholders,
not `N/A`):

| Field | Rule |
|---|---|
| Title | One line naming what is broken and where |
| Description | What is wrong and its impact |
| Severity | One of the levels in the severity guide below |
| Environment | Dev, QA, Staging, UAT, or Production |
| Build | A specific build or version number |
| Steps to reproduce | Numbered, one action per step, starting from the preconditions |
| Expected result | What should happen |
| Actual result | What happens instead |
| Reproducibility | Written as `successes/attempts`, e.g. `3/5` |

Every other field is optional. Fill it in when the user has given the information,
otherwise write `N/A`. Never delete a field.

## Workflow

1. **Blank template requested.** If the user only wants the template, give them the
   contents of `templates/defect-template.md` (or copy the file to where they ask)
   and stop.
2. **Collect.** Pull every detail you can from what the user has already said,
   pasted, or attached (logs, screenshots, error text). Do not ask for things you
   already have.
3. **Ask for the gaps.** If any mandatory field is missing, ask for all the missing
   ones in a single message. Do not invent values for mandatory fields. Optional
   fields may be left as `N/A` without asking.
4. **Write.** Fill in the template. Tighten the wording, but keep the user's facts.
   - Steps: numbered, imperative, one action each ("Tap **Checkout**").
   - Actual result: quote error messages exactly.
   - Date & time: if not given, use the current date and time with the timezone.
5. **Check before handing back.** Confirm each mandatory field has a real value,
   the severity matches the guide, and logs and account fields contain no secrets.
6. **Deliver.** Show the report as Markdown. If the user asks for a file, save it as
   `defect-<short-slug>.md`, or wherever they ask.

## Severity guide

| Severity | Use when |
|---|---|
| Blocker | Stops testing or release; app crashes on launch, core flow fully down, data loss, security hole |
| Critical | A core feature is broken with no workaround |
| Major | A feature is broken but a workaround exists, or a non-core feature is fully broken |
| Minor | Small functional problem with little user impact |
| Trivial | Cosmetic: typo, alignment, colour |

If the user's chosen severity clearly doesn't match the guide, say so once and
suggest a level, but keep theirs if they confirm it.

## Defect type

- **UI**: wrong layout, text, or behaviour in the client while the API response is correct.
- **Backend**: the API returns a wrong status, wrong data, or an error.
- **UI + Backend**: both sides are wrong.
- **Unknown**: not yet determined. Suggest checking the API logs to tell which.

## Sensitive data

Before writing logs or account details into the report, mask passwords, auth
tokens, API keys, session cookies, and personal data (emails, phone numbers,
card numbers), e.g. `Authorization: Bearer ****`. In the Account field, give only
the username or user ID, never the password.
