# Contributing to MyZubster

Thank you for your interest in contributing to the MyZubster ecosystem! This guide covers how to contribute, how our automation works, and how to work with bots.

---

## 🤖 Automation in this project

MyZubster uses automation to help manage the large volume of issues and PRs across our repositories.

### What is automated?

- **Issue triage and labeling** — new issues are automatically categorized and labeled
- **PR validation** — tests, linting, and format checks run on every pull request
- **Bounty status tracking** — bounty issues are monitored and status updates are posted automatically
- **Reminder comments** — automated reminders keep contributors and maintainers informed

### How to identify automation

- Comments from **@myzubster-bot** are automated
- The `automated` label indicates a bot-generated comment or action
- Automated comments always include a disclaimer noting they are machine-generated

### Human review

Despite automation, every PR is reviewed by a human maintainer before merge. Bounty payments are manually approved and processed. Automation assists — it does not replace — human judgment.

### Tips for contributors

- Don't worry if a bot comments on your PR — it's just running checks
- If you need human attention, ping a maintainer directly
- Bot comments are for information, not decisions

---

## 🔧 Working with bots

### Bounty monitoring

Our cron-based bounty monitor scans all MyZubster repositories hourly for new bounty issues. When a new bounty is found, it analyzes the task and posts a claim comment with the XMR payment address.

### PR checks

Every PR triggers automated CI checks:
- Lint and syntax validation
- Test suite execution
- Mergeability verification

If a check fails, review the logs to understand the root cause before re-running.

### Issue management

Issues are automatically labeled based on their content and repository. Bounty issues include payment amounts and XMR addresses for reference.

---

## 📋 Quick start

1. Fork the repository
2. Create a feature branch (`git checkout -b feat/your-feature`)
3. Make your changes
4. Commit with a clear message
5. Push to your fork and open a PR
6. Wait for CI checks and human review

---

## 📌 Notes

- This project uses XMR (Monero) for bounty payments
- All bounty payout addresses are verified against the project's official address on file
- Please read the issue description carefully before claiming a bounty
- Quality over quantity — deliver clean, well-documented work

---

*Last updated: 2026-08-03*
