# GitHub Changelog — Week 17, 2026

> **Period:** 2026-04-19 to 2026-04-25
> **Source:** https://github.blog/changelog/

---

## GitHub Copilot (AI)

### GPT-5.5 is generally available for GitHub Copilot

**Published:** 2026-04-24
**Source:** https://github.blog/changelog/2026-04-24-gpt-5-5-is-generally-available-for-github-copilot
**Category:** GitHub Copilot (AI)

### Summary

GPT-5.5, OpenAI's latest model, is now rolling out on GitHub Copilot for Pro+, Business, and Enterprise subscribers, delivering its strongest performance on complex, multi-step agentic coding tasks. The model resolves real-world coding challenges that previous GPT models couldn't handle and launches with a 7.5× premium request multiplier as part of promotional pricing. It is available in VS Code, Visual Studio, JetBrains, Xcode, Eclipse, Copilot CLI, GitHub Mobile, and github.com. Enterprise and Business administrators must enable the GPT-5.5 policy in Copilot settings before users can select it.

### Additional Resources

- [Supported AI models in GitHub Copilot](https://docs.github.com/en/copilot/reference/ai-models/supported-models) — Official docs listing all supported AI models, their availability per plan, and premium request multipliers.
- [GitHub Copilot plans](https://github.com/features/copilot/plans) — Overview of Copilot subscription tiers that include access to GPT-5.5.
- [GitHub Community — Copilot Conversations](https://github.com/orgs/community/discussions/categories/copilot-conversations) — Community forum for sharing feedback and experiences with GitHub Copilot features.

---

### Inline agent mode in preview and more in GitHub Copilot for JetBrains IDEs

**Published:** 2026-04-24
**Source:** https://github.blog/changelog/2026-04-24-inline-agent-mode-in-preview-and-more-in-github-copilot-for-jetbrains-ides
**Category:** GitHub Copilot (AI)

### Summary

GitHub Copilot for JetBrains IDEs now offers inline agent mode in public preview, bringing agentic capabilities directly into the inline chat experience via Shift+Ctrl/Cmd+I without switching to the chat panel. Next Edit Suggestions gains inline edit previews and a far-away edit gutter indicator for navigating suggestions across multiple screens. This release also adds global auto-approve for tool calls plus granular controls for terminal commands and file edits, along with a range of UX and stability improvements. Business and Enterprise subscribers require an administrator to enable the Editor preview features policy before using these features.

### Additional Resources

- [GitHub Copilot for JetBrains plugin](https://plugins.jetbrains.com/plugin/17718-github-copilot--your-ai-pair-programmer) — JetBrains Marketplace page for installing the latest version of the GitHub Copilot plugin.
- [GitHub Copilot for JetBrains feedback repository](https://github.com/microsoft/copilot-intellij-feedback/issues) — Community issues and feedback tracker for the JetBrains Copilot plugin.

---

### Better debugging with GitHub Copilot on the web

**Published:** 2026-04-23
**Source:** https://github.blog/changelog/2026-04-23-better-debugging-with-github-copilot-on-the-web
**Category:** GitHub Copilot (AI)

### Summary

GitHub Copilot Chat on github.com now provides structured root-cause analysis when you paste a stack trace, helping you move from "where it crashed" to "why it happened." Responses are organized to show what failed and where, the violated assumption, the most likely root cause with code evidence, a confidence level, a suggested fix, and next checks when verification is needed. No configuration is required; this feature is available to all Copilot users on github.com. Adding a repro step or related file context produces even faster root-cause analysis.

### Additional Resources

- [Asking GitHub Copilot questions on GitHub.com](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat/asking-github-copilot-questions-in-githubcom) — Official guide to using Copilot Chat on the GitHub web interface, including adding repository and file context.
- [GitHub Copilot documentation](https://docs.github.com/en/copilot) — Main Copilot documentation hub covering all features, plans, and IDE integrations.

---

### Copilot Chat improvements for pull requests

**Published:** 2026-04-23
**Source:** https://github.blog/changelog/2026-04-23-copilot-chat-improvements-for-pull-requests
**Category:** GitHub Copilot (AI)

### Summary

GitHub Copilot Chat now provides richer context and new capabilities when working with diffs and pull requests on github.com. Three new abilities are available—pull request understanding (including comments, commits, file changes, and reviews), pull request review, and pull request summarization—accessible via github.com/copilot or the global Copilot navigation. Public-preview-enabled users can also click the Copilot button on a diff to ask questions about the changes. Suggested prompts like "Help review this pull request" guide you through the relevant functionality.

### Additional Resources

- [About pull request reviews](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews) — Overview of the pull request review workflow, including how approvals and change requests work on GitHub.
- [GitHub Community discussion on Copilot Chat for PRs](https://github.com/orgs/community/discussions/193348) — Community discussion thread for sharing feedback on Copilot Chat improvements for pull requests.

---

### Copilot cloud agent fields added to usage metrics

**Published:** 2026-04-23
**Source:** https://github.blog/changelog/2026-04-23-copilot-cloud-agent-fields-added-to-usage-metrics
**Category:** GitHub Copilot (AI)

### Summary

Following the rename of Copilot coding agent to Copilot cloud agent, the Copilot usage metrics API now includes the new `used_copilot_cloud_agent` boolean field in user-level reports. This field mirrors the existing `used_copilot_coding_agent` flag and is available in both single-day and 28-day rolling window reports at enterprise and organization levels. Both fields return the same value and coexist, allowing teams to migrate at their own pace. The legacy `used_copilot_coding_agent` field will be deprecated on August 1, 2026.

### Additional Resources

- [GitHub Copilot usage metrics](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics) — Documentation explaining how to interpret and use Copilot usage metrics across dashboards and APIs.
- [Copilot usage metrics REST API reference](https://docs.github.com/enterprise-cloud@latest/rest/copilot/copilot-usage-metrics) — REST API reference for retrieving Copilot usage metrics at enterprise and organization levels.

---

## Code Versioning (Repositories + Git)

### Disable commit comments across your organization

**Published:** 2026-04-23
**Source:** https://github.blog/changelog/2026-04-23-disable-commit-comments-across-your-organization
**Category:** Code Versioning (Repositories + Git)

### Summary

Organization owners can now disable commit comments for all repositories in their organization from a single setting, eliminating the need to configure each repository individually. This extends the previously released per-repository commit comment control to the organization level, found under **Organization Settings → Repository → General → Commit comments → Disabled by default**. The change is especially valuable for organizations managing large numbers of repositories. A Community discussion is open for feedback on this new capability.

### Additional Resources

- [Managing organization settings on GitHub](https://docs.github.com/en/organizations/managing-organization-settings) — Overview of settings available to organization owners for controlling repository-level behaviors across their organization.
- [GitHub Community discussion on disabling commit comments](https://github.com/orgs/community/discussions/193350) — Community feedback thread for the new organization-level commit comment control.

---

## Pull Requests

### Global pull requests dashboard moves to opt-out public preview

**Published:** 2026-04-23
**Source:** https://github.blog/changelog/2026-04-23-global-pull-requests-dashboard-moves-to-opt-out-public-preview
**Category:** Pull Requests

### Summary

The new global pull requests dashboard is now on by default for all GitHub users as it transitions to opt-out public preview, providing a unified place to manage all pull requests. New capabilities include a configurable default view, inbox filtering by org, dedicated "Your drafts" and "Waiting for review" sections, a team review section, expandable/collapsible groups, and improvements to the PR list such as open/closed toggles, unread indicators, and inline status check visibility. Users can opt out at any time via the **Preview** label at the top of the page or through Feature Preview settings. Durable URLs for saved views ensure bookmarks remain stable after edits.

### Additional Resources

- [Viewing all of your issues and pull requests](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/viewing-all-of-your-issues-and-pull-requests) — Official documentation on using the global pull request and issue dashboards, including saved views and filtering.
- [Exploring early access releases with feature preview](https://docs.github.com/en/get-started/using-github/exploring-early-access-releases-with-feature-preview) — Guide to managing early access features in GitHub, including how to opt in or out of preview features.

---

## Security (Dependabot / Code Scanning)

### Dependabot-based dependency graphs for Python

**Published:** 2026-04-23
**Source:** https://github.blog/changelog/2026-04-23-dependabot-graphs-for-python
**Category:** Security (Dependabot / Code Scanning)

### Summary

Python projects now benefit from more complete and accurate transitive dependency trees in their dependency graphs and Software Bills of Materials (SBOMs), powered by a new Dependabot job type that builds and uploads dependency snapshots. This approach supports pip, uv, and Poetry (v1 and v2) and leverages organization-wide configurations for private registries without incurring additional Actions minutes charges. It is similar to dependency autosubmission but uses Dependabot's broader access to registry configuration for more reliable results.

### Additional Resources

- [Configuring the dependency graph](https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/configuring-the-dependency-graph) — Official guide to enabling and managing GitHub's dependency graph for repositories and organizations.
- [About the dependency graph](https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph) — Overview of how GitHub's dependency graph works, which ecosystems it supports, and how SBOMs are generated.
- [Using the dependency submission API](https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/using-the-dependency-submission-api) — Reference for the API used to submit dependency snapshots programmatically, which underpins this Dependabot feature.

---

## Social Features (Stars, Forks, Watch)

### Changes to notification retention and archived repository watches

**Published:** 2026-04-24
**Source:** https://github.blog/changelog/2026-04-24-changes-to-notification-retention-and-archived-repository-watches
**Category:** Social Features (Stars, Forks, Watch)

### Summary

Two behavioral changes are rolling out for GitHub notifications and repository watches over the coming months. Web notification retention is being reduced from five months to three months to keep inboxes focused on recent activity; email notifications are not affected. Additionally, watches on repositories archived for more than six months will be automatically removed for non-collaborators, since archived repos are read-only and cannot generate new notifications. Repository owners, organization members, direct collaborators, and team members with access will retain their watches.

### Additional Resources

- [Configuring notifications](https://docs.github.com/en/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications) — Official guide to configuring GitHub notification delivery, types, and retention settings.
- [Viewing your subscriptions](https://docs.github.com/en/account-and-profile/managing-subscriptions-and-notifications-on-github/managing-subscriptions-for-activity-on-github/viewing-your-subscriptions) — Documentation on reviewing and managing your repository watches and notification subscriptions.

---

## Others

### Notice about upcoming new format for GitHub App installation tokens

**Published:** 2026-04-24
**Source:** https://github.blog/changelog/2026-04-24-notice-about-upcoming-new-format-for-github-app-installation-tokens
**Category:** Others

### Summary

Starting April 27, 2026, GitHub is rolling out a new stateless token format for GitHub App installation tokens that improves performance and API reliability at scale. Newly issued tokens will be approximately 520 characters long (up from 40) and will use the format `ghs_APPID_JWT`, while still retaining the `ghs_` prefix. Developers should ensure their apps treat tokens as opaque strings, avoid length assumptions, remove regex patterns like `ghs_[A-Za-z0-9]{36}`, and ensure database columns can store at least 520 characters. The rollout covers GitHub Actions `GITHUB_TOKEN` and first-party integrations from April 27 to mid-May, with broader rollout through late June 2026.

### Additional Resources

- [Authenticating as a GitHub App installation](https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/authenticating-as-a-github-app-installation) — Official docs explaining how GitHub App installation access tokens work and how to use them for API authentication.
- [About GitHub's token formats](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github#githubs-token-formats) — Reference for all GitHub token type prefixes and their intended use cases.
- [GitHub Community announcements](https://github.com/orgs/community/discussions/categories/announcements) — Official GitHub announcements channel with migration guidance for the new token format change.
