# Agents

This repository is watched by the superagent account `mbp-dsh`. Work starts when `tyler-jewell` mentions `@mbp-dsh` on an issue.

The worker checks out `/var/lib/dsh/src/<owner>/<name>` on a branch `agent/<ticket short name>` and opens a pull request. The pull request body contains `Fixes #<number>`. The worker does not merge. A person, or an agent session in `/Users/mbp/workspaces/dsh-superagent`, merges with the host `gh` account (`gh pr merge <number> --merge`).

After the pull request is open, report progress and stop. Do not report ready, and do not pass `pr_number`. The report tool only accepts a pull request on the control repository. This ticket ends when its pull request merges.

The worker does not delete this repository and does not change its visibility. The worker does not run `cf` and does not deploy.

Rules that belong only to this project stay in this file.
