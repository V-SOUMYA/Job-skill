# us-job-agent (Soumya)

Status: **initialized, dry-run mode, manual trigger only** (no scheduled or background runs; say "Run us-job-agent"). Nothing is submitted or emailed until you switch `mode: live`
in `config/job_preferences.yaml` and confirm it in chat.

| Piece | State |
|---|---|
| Candidate profile (`config/candidate_profile.yaml`) | Built from master resume only; private details not provided → affected applications marked "Needs my input" |
| Eligibility gates (full-time, US, ≤500 employees, ≤5 days, open, auth conflicts) | Working, tested |
| Scoring 30/25/20/15/10, 65% threshold | Working, tested (judgment parts require evidence) |
| Dedup, AI-trap detection, daily caps (15/15), truthfulness check | Working, tested |
| `job_tracker.xlsx` (all spec columns + History sheet) | Created |
| Discovery: Greenhouse/Lever/Ashby/career pages/YC/ZipRecruiter/Indeed/HiringCafe | Via web search + fetch |
| Discovery: LinkedIn/Wellfound/Jobright/Handshake | Login required — only via your signed-in browser |
| Gmail monitoring | Scoped query + classifier; read-only, no auto replies |
| Apollo / Hunter outreach | **Disabled** — no API keys |
| Auto-submission | Disabled (dry-run). Many ATS forms have CAPTCHAs → "Manual submission required" |

Run tests: `python -m pytest -q tests` · Procedure: `RUNBOOK.md`
State (tracker, history, daily caps) carries over via the updated zip delivered after each run.

