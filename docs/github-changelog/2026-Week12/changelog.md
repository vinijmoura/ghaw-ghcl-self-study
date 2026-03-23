# GitHub Changelog — Week 12, 2026

> **Period:** 2026-03-15 to 2026-03-21
> **Source:** https://github.blog/changelog/

---

## GitHub Actions (CI/CD)

### GitHub Actions: Late March 2026 updates

**Published:** 2026-03-19
**Source:** https://github.blog/changelog/2026-03-19-github-actions-late-march-2026-updates
**Category:** GitHub Actions (CI/CD)

### Summary

GitHub Actions introduces two quality-of-life improvements this month. Developers can now use environments in workflows without triggering automatic deployments by setting `deployment: false` — useful for accessing environment secrets and variables without creating deployment records. Additionally, IANA timezone support is now available for scheduled workflows, allowing `cron` triggers to run at a local time rather than being locked to UTC.

### Additional Resources

- [Using environments for deployment](https://docs.github.com/en/actions/deployment/targeting-different-environments/using-environments-for-deployment) — Official guide on creating and securing GitHub Actions deployment environments with protection rules and secrets.
- [Workflow syntax for GitHub Actions](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions) — Complete reference for GitHub Actions YAML workflow syntax, including the `on.schedule` trigger and the new `timezone` field.
- [GitHub Actions community discussions](https://github.com/orgs/community/discussions/categories/actions) — Community forum where you can join discussions and share feedback on GitHub Actions features.

---

### Actions Runner Controller release 0.14.0

**Published:** 2026-03-19
**Source:** https://github.blog/changelog/2026-03-19-actions-runner-controller-release-0-14-0
**Category:** GitHub Actions (CI/CD)

### Summary

Actions Runner Controller (ARC) 0.14.0 is now generally available, introducing several powerful improvements for self-hosted Kubernetes runners. Runner scale sets can now carry multiple labels, eliminating the need to create separate scale sets for each attribute combination. ARC now uses the open-source `actions/scaleset` library as its sole API client, and supports custom Kubernetes labels and annotations on internally managed resources. The listener pod also now defaults to Linux nodes in mixed-OS clusters, preventing scheduling failures on Windows.

### Additional Resources

- [About Actions Runner Controller](https://docs.github.com/actions/hosting-your-own-runners/managing-self-hosted-runners-with-actions-runner-controller/about-actions-runner-controller) — Official documentation explaining ARC's architecture, how it orchestrates self-hosted runners with Kubernetes, and how autoscaling works.
- [actions/scaleset (GitHub)](https://github.com/actions/scaleset) — The publicly available Go library used by ARC to communicate with GitHub Actions service APIs, also usable for building custom autoscaling solutions.
- [ARC Helm chart releases](https://github.com/actions/actions-runner-controller/releases) — Official release history for the ARC Helm charts, including the 0.14.0 release notes and experimental chart updates.

---

## GitHub Copilot (AI)

### Copilot usage metrics now resolve auto model selection to actual models

**Published:** 2026-03-20
**Source:** https://github.blog/changelog/2026-03-20-copilot-usage-metrics-now-resolve-auto-model-selection-to-actual-models
**Category:** GitHub Copilot (AI)

### Summary

When auto model selection is enabled, Copilot usage metrics previously grouped activity under a generic "Auto" label. Activity now resolves to the actual model name, giving admins a complete view of which models their teams are using. This applies to the `totals_by_model_feature` breakdown in the Copilot usage metrics REST API and dashboard at the enterprise, org, and user levels. A separate breakdown of auto vs. manually selected model usage is planned for a future update.

### Additional Resources

- [Copilot usage metrics REST API](https://docs.github.com/enterprise-cloud@latest/rest/copilot/copilot-usage-metrics?apiVersion=2026-03-10) — Reference for the REST API endpoints that expose Copilot usage data, including model-level breakdowns at the enterprise, org, and user levels.
- [Viewing GitHub Copilot usage metrics](https://docs.github.com/copilot/rolling-out-github-copilot-at-scale/measuring-the-impact-of-github-copilot) — Guide on how administrators can measure Copilot's impact and review usage dashboards across an organization.
- [GitHub Copilot plans and features](https://github.com/features/copilot/plans) — Overview of Copilot subscription tiers and the features available at each level, including admin dashboards and usage reporting.

---

### Trace any Copilot coding agent commit to its session logs

**Published:** 2026-03-20
**Source:** https://github.blog/changelog/2026-03-20-trace-any-copilot-coding-agent-commit-to-its-session-logs
**Category:** GitHub Copilot (AI)

### Summary

Copilot coding agent commits are co-authored by Copilot and the human who delegated the task. A new `Agent-Logs-Url` trailer is now included in every agent-authored commit message, providing a permanent link back to the full session logs. This makes it easy to understand why Copilot made a change during code review or to trace agent activity for compliance and auditing purposes.

### Additional Resources

- [Tracking GitHub Copilot's sessions](https://docs.github.com/copilot/how-tos/use-copilot-agents/coding-agent/track-copilot-sessions) — Official documentation on how to track Copilot coding agent sessions via the agents panel, Raycast, VS Code, and session logs.
- [About GitHub Copilot coding agent](https://docs.github.com/copilot/concepts/agents/coding-agent/about-coding-agent) — Overview of how Copilot coding agent works, including how it creates pull requests and integrates with your development environment.
- [Enabling Copilot coding agent (Enterprise)](https://docs.github.com/enterprise-cloud@latest/copilot/how-tos/agents/copilot-coding-agent/enabling-copilot-coding-agent) — Steps for Copilot Business and Enterprise administrators to enable coding agent from the Policies page.

---

### Monitor Copilot coding agent logs live in Raycast

**Published:** 2026-03-20
**Source:** https://github.blog/changelog/2026-03-20-monitor-copilot-coding-agent-logs-live-in-raycast
**Category:** GitHub Copilot (AI)

### Summary

The GitHub Copilot extension for Raycast now lets you watch Copilot coding agent session logs in real time without switching to GitHub.com. Using the **View Tasks** command in Raycast, you can pick an active session and see live log output with just a few keystrokes. This feature is available to Copilot Pro, Pro+, Business, and Enterprise subscribers with the coding agent enabled.

### Additional Resources

- [GitHub Copilot extension for Raycast](https://www.raycast.com/github/github-copilot) — The official Raycast extension page for GitHub Copilot, where you can install it and see available commands including task management and live log viewing.
- [Tracking GitHub Copilot's sessions](https://docs.github.com/copilot/how-tos/use-copilot-agents/coding-agent/track-copilot-sessions) — Documentation covering all supported ways to monitor agent sessions, including Raycast, VS Code, and the GitHub CLI.
- [About GitHub Copilot coding agent](https://docs.github.com/copilot/concepts/agents/coding-agent/about-coding-agent) — Introduction to Copilot coding agent's capabilities and how to delegate tasks to it from various surfaces.

---

### More visibility into Copilot coding agent sessions

**Published:** 2026-03-19
**Source:** https://github.blog/changelog/2026-03-19-more-visibility-into-copilot-coding-agent-sessions
**Category:** GitHub Copilot (AI)

### Summary

The Copilot coding agent session logs have been improved with three key visibility enhancements. Built-in setup steps (repository cloning and firewall startup) and custom setup steps defined via `copilot-setup-steps.yml` now appear in the logs with start/finish markers. When Copilot delegates work to subagents, their activity is collapsed by default with a heads-up display showing current progress, while still being expandable for full detail.

### Additional Resources

- [About GitHub Copilot coding agent](https://docs.github.com/copilot/concepts/agents/coding-agent/about-coding-agent) — Overview of how Copilot coding agent operates, including its use of subagents for research and code modification tasks.
- [Customizing the agent environment](https://docs.github.com/enterprise-cloud@latest/copilot/how-tos/use-copilot-agents/coding-agent/customize-the-agent-environment) — Guide on using `copilot-setup-steps.yml` to define custom setup steps that run before Copilot starts working on a task.
- [Tracking GitHub Copilot's sessions](https://docs.github.com/copilot/how-tos/use-copilot-agents/coding-agent/track-copilot-sessions) — Documentation on reading session logs and monitoring agent progress from GitHub, Raycast, VS Code, and the CLI.

---

### Copilot coding agent now starts work 50% faster

**Published:** 2026-03-19
**Source:** https://github.blog/changelog/2026-03-19-copilot-coding-agent-now-starts-work-50-faster
**Category:** GitHub Copilot (AI)

### Summary

GitHub has optimized Copilot coding agent's startup time, cutting it by 50%. This means the agent reaches working state more quickly whether you assign it an issue, open a prompt from the Agents tab, or mention `@copilot` in a pull request comment. Faster startup translates to quicker pull request creation and shorter feedback loops when iterating on changes.

### Additional Resources

- [Asking GitHub Copilot to create a pull request](https://docs.github.com/copilot/how-tos/use-copilot-agents/coding-agent/create-a-pr) — Documentation on all the ways you can delegate tasks to Copilot coding agent to open new pull requests.
- [Asking Copilot to make changes to an existing pull request](https://docs.github.com/copilot/how-tos/use-copilot-agents/coding-agent/make-changes-to-an-existing-pr) — Guide on using `@copilot` in pull request comments to trigger iterative changes from the coding agent.
- [About GitHub Copilot coding agent](https://docs.github.com/copilot/concepts/agents/coding-agent/about-coding-agent) — Overview of the coding agent's capabilities, available plans, and how it compares to traditional AI-assisted workflows.

---

## Pull Requests

### View code and comments side-by-side in pull request Files changed page

**Published:** 2026-03-19
**Source:** https://github.blog/changelog/2026-03-19-view-code-and-comments-side-by-side-in-pull-request-files-changed-page
**Category:** Pull Requests

### Summary

Docked panels are rolling out for the pull request "Files changed" page, allowing reviewers to keep key context open alongside the diff. Four panels are now available: **Comments** (all review and conversation threads), **Overview** (PR description and goals), **Merge status** (approvals, checks, and blockers), and **Alerts** (code scanning findings). Reviewers on the classic view must opt into the new experience first.

### Additional Resources

- [Reviewing proposed changes in a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/reviewing-proposed-changes-in-a-pull-request) — Official guide on how to review diffs, leave comments, and submit approvals in GitHub pull requests.
- [Improved pull request Files changed page (on by default)](https://github.blog/changelog/2026-01-22-improved-pull-request-files-changed-page-on-by-default/) — Changelog post announcing the new Files changed experience that the docked panels build upon.
- [Docked panels feedback discussion](https://gh.io/docked-panels-feedback) — Community feedback thread for reporting issues, asking questions, and reviewing known issues with the new docked panels feature.

---

## Codespaces

### Codespaces with data residency now available in Japan

**Published:** 2026-03-19
**Source:** https://github.blog/changelog/2026-03-19-codespaces-with-data-residency-now-available-in-japan
**Category:** Codespaces

### Summary

GitHub Codespaces data residency now includes Japan as a supported region, joining the existing EU and Australia regions. This public preview availability means enterprises hosted in the Japan region can create and manage codespaces while keeping data local. This follows the January 2026 announcement of Codespaces entering public preview for GitHub Enterprise with data residency.

### Additional Resources

- [GitHub Codespaces overview](https://docs.github.com/en/codespaces/overview) — Introduction to GitHub Codespaces, including how cloud-based dev environments work and how to connect from a browser, VS Code, or the CLI.
- [Codespaces in public preview for GitHub Enterprise with data residency](https://github.blog/changelog/2026-01-29-codespaces-is-now-in-public-preview-for-github-enterprise-with-data-residency/) — Original changelog announcement of Codespaces data residency entering public preview, listing initially supported regions.
- [GitHub Codespaces documentation](https://docs.github.com/codespaces) — Full documentation hub for Codespaces, covering setup, configuration, billing, and organization management.

---

## Others

### A smoother navigation experience in GitHub Mobile for Android

**Published:** 2026-03-20
**Source:** https://github.blog/changelog/2026-03-20-a-smoother-navigation-experience-in-github-mobile-for-android
**Category:** Others

### Summary

GitHub Mobile for Android has received a navigation overhaul designed for a more consistent and intuitive user experience. Moving between Home and Inbox is now smoother, the bottom navigation bar is more consistently available, and each tab better preserves your scroll position as you move between them. The update is available in the latest production build on the Google Play Store.

### Additional Resources

- [GitHub Mobile on Google Play](https://play.google.com/store/apps/details?id=com.github.android) — Official GitHub Mobile app page on the Google Play Store, where you can install or update to the latest version with the improved navigation.
- [GitHub Mobile documentation](https://docs.github.com/en/get-started/using-github/github-mobile) — Overview of GitHub Mobile features, supported platforms, and how to manage notifications and code review on the go.
- [GitHub Mobile community discussions](https://github.com/orgs/community/discussions/categories/mobile) — Community forum for GitHub Mobile feedback, bug reports, and announcements about upcoming changes.

---
