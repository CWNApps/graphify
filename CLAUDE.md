# graphify (CWNApps fork)

## GitHub Actions cost rules (founder standing rule, 2026-11-07, restated 2026-11-20 when spend passed $250)

GitHub Actions minutes cost real money. Follow these in every session. Never weaken a required check to save money; save by running less often.
The full text lives in the cwn-trust-gate CLAUDE.md.

1. Run tests inside your own session before pushing (`python -m pytest tests/ -q`, print only failures and the summary line).
2. Keep a PR in draft while iterating. Mark it ready once, with one batched push. After that, push only to fix a failing check.
3. Every push to a ready PR restarts its checks; batch fixes into one push. Never push an empty commit or close and reopen a PR to kick CI.
4. Do not dispatch a workflow on a feature branch to test a draft.
5. A new or changed workflow needs a `concurrency` block that cancels superseded PR runs, a `timeout-minutes` on every job, and `retention-days` on debugging artifacts.
6. No cron more often than hourly, no macOS runners, and Windows runners only by hand, unless the founder approves it.
7. The Actions budget is a ceiling the founder sets in GitHub billing. Never ask him to raise it as a fix for usage.
