# GitHub Changelog — Week 13, 2026

> **Period:** 2026-03-22 to 2026-03-28
> **Source:** https://github.blog/changelog/

---

## GitHub Actions (CI/CD)

### Custom images for GitHub-hosted runners are now generally available

**Published:** 2026-03-26
**Source:** https://github.blog/changelog/2026-03-26-custom-images-for-github-hosted-runners-are-now-generally-available
**Category:** GitHub Actions (CI/CD)

### Summary

Custom images for GitHub-hosted runners have graduated from public preview (first introduced in October 2025) to general availability. This feature allows organizations to start from a GitHub-curated base image and build their own virtual machine image with preinstalled tools, dependencies, certificates, and configurations. The result is faster, more consistent, and more secure workflows, with reduced setup overhead. Existing public-preview users require no action — current images and workflows continue to work as-is.

### Additional Resources

- [Using custom images (GitHub Docs)](https://docs.github.com/en/actions/how-tos/manage-runners/larger-runners/use-custom-images) — Step-by-step guide covering how to set up an image-generation runner, generate a custom image, and attach it to a hosted runner.
- [Managing larger runners (GitHub Docs)](https://docs.github.com/en/actions/how-tos/manage-runners/larger-runners/manage-larger-runners) — Reference documentation for creating, configuring, and governing larger runners, including custom-image policies for enterprise owners.
- [About GitHub-hosted runners (GitHub Docs)](https://docs.github.com/en/actions/concepts/runners/github-hosted-runners) — Overview of GitHub-hosted runner options and their runner images, including how custom images extend the standard offering.

---

### View Agentic Workflow configs in the Actions run summary

**Published:** 2026-03-26
**Source:** https://github.blog/changelog/2026-03-26-view-agentic-workflow-configs-in-the-actions-run-summary
**Category:** GitHub Actions (CI/CD)

### Summary

GitHub Actions run summaries for agentic workflows now display the Agentic Workflow markdown configuration file that was active when the run executed. This improvement reduces the need to navigate away from the run summary to a separate file view and makes it easy to verify the exact configuration that drove a given run. The feature is available to all repositories using GitHub Agentic Workflows.

### Additional Resources

- [GitHub Agentic Workflows documentation](https://github.github.com/gh-aw/) — Official documentation covering the concepts, configuration format, and capabilities of GitHub Agentic Workflows.
- [Agentic Workflows quick-start guide](https://github.github.com/gh-aw/setup/quick-start/) — A hands-on quick-start that walks you through setting up your first agentic workflow from scratch.

---

## GitHub Copilot (AI)

### Ask @copilot to resolve merge conflicts on pull requests

**Published:** 2026-03-26
**Source:** https://github.blog/changelog/2026-03-26-ask-copilot-to-resolve-merge-conflicts-on-pull-requests
**Category:** GitHub Copilot (AI)

### Summary

The Copilot coding agent can now resolve merge conflicts on pull requests when you mention `@copilot` in a PR comment with a natural-language instruction such as "@copilot Merge in main and resolve the conflicts." The agent works in a cloud-based development environment, resolves conflicts, verifies that the build and tests still pass, and then pushes the changes and requests your review. This capability is available on all paid Copilot plans; Copilot Business and Enterprise users require an administrator to enable the coding agent first.

### Additional Resources

- [Asking Copilot to make changes to an existing pull request (GitHub Docs)](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/make-changes-to-an-existing-pr) — Covers how to use `@copilot` in PR comments to trigger merge-conflict resolution, test fixes, and other code changes.
- [About GitHub Copilot coding agent (GitHub Docs)](https://docs.github.com/en/copilot/concepts/about-copilot-coding-agent) — Explains the architecture and capabilities of the Copilot coding agent, including how it creates and manages its own development environment.
- [Enabling Copilot coding agent for Business and Enterprise (GitHub Docs)](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/agents/coding-agent/coding-agent-for-business-and-enterprise) — Administrator guide for enabling the Copilot coding agent within organizations on Business and Enterprise plans.

---

### Gemini 3 Pro deprecated

**Published:** 2026-03-26
**Source:** https://github.blog/changelog/2026-03-26-gemini-3-pro-deprecated
**Category:** GitHub Copilot (AI)

### Summary

Gemini 3 Pro has been deprecated across all GitHub Copilot experiences — including Copilot Chat, inline edits, ask and agent modes, and code completions — effective March 26, 2026. GitHub recommends migrating workflows to Gemini 3.1 Pro as the suggested alternative. Copilot Enterprise administrators may need to update their model policies to enable the replacement model; no action is required to remove the deprecated model itself.

### Additional Resources

- [Supported AI models in GitHub Copilot (GitHub Docs)](https://docs.github.com/en/copilot/reference/ai-models/supported-models) — Lists all currently supported and recently retired AI models available in Copilot, including retirement dates and recommended alternatives.
- [Changing the AI model for GitHub Copilot Chat (GitHub Docs)](https://docs.github.com/en/copilot/how-tos/use-ai-models/change-the-chat-model) — Instructions for selecting a different model in Copilot Chat across IDEs and GitHub.com.

---

### GitHub Copilot for Jira — Public preview enhancements

**Published:** 2026-03-25
**Source:** https://github.blog/changelog/2026-03-25-github-copilot-for-jira-public-preview-enhancements
**Category:** GitHub Copilot (AI)

### Summary

The GitHub Copilot coding agent integration for Jira has received several improvements based on early adopter feedback: clearer onboarding error messages and extended documentation, the ability to specify which AI model to use directly from a Jira comment, automatic inclusion of the Jira ticket number in the pull request title and branch name, and the ability to supply Confluence page context to the agent via the Atlassian MCP server. Users must update to the latest version of the GitHub Copilot for Jira app from the Atlassian Marketplace to receive these enhancements.

### Additional Resources

- [Integrating Copilot coding agent with Jira (GitHub Docs)](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/integrate-coding-agent-with-jira) — Full setup and usage guide for connecting Copilot coding agent to a Jira Cloud workspace, including prerequisites and installation steps.
- [Extending Copilot coding agent with MCP (GitHub Docs)](https://docs.github.com/en/copilot/customizing-copilot/extending-copilot-coding-agent-with-mcp) — Explains how to configure MCP servers (such as the Atlassian MCP server) to give the coding agent access to external tools and context sources like Confluence.
- [GitHub Copilot for Jira on Atlassian Marketplace](https://marketplace.atlassian.com/apps/1582455624) — The official app listing where administrators can install or update the GitHub Copilot for Jira integration for their Atlassian instance.

---

### Copilot usage metrics now identify active Copilot coding agent users

**Published:** 2026-03-25
**Source:** https://github.blog/changelog/2026-03-25-copilot-usage-metrics-now-identify-active-copilot-coding-agent-users
**Category:** GitHub Copilot (AI)

### Summary

Enterprise and organization administrators can now see which users have active Copilot coding agent (CCA) sessions in the daily and 28-day Copilot usage metrics reports. A new `used_copilot_coding_agent` field in the API response tracks whether a user triggered a CCA session by assigning Copilot to an issue or by tagging `@copilot` in a pull request comment. This allows admins to distinguish between IDE agent mode usage and coding agent usage, providing a more complete picture of Copilot adoption beyond the IDE.

### Additional Resources

- [About Copilot usage metrics (GitHub Docs)](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics) — Overview of all available Copilot metrics surfaces: the API, the usage dashboard, the code generation dashboard, and NDJSON export.
- [Copilot usage metrics REST API (GitHub Docs)](https://docs.github.com/en/enterprise-cloud@latest/rest/copilot/copilot-usage-metrics?apiVersion=2026-03-10) — API reference for the enterprise and organization usage metrics endpoints, including the new `used_copilot_coding_agent` field.

---

## Pull Requests

### New pull requests dashboard is in public preview

**Published:** 2026-03-26
**Source:** https://github.blog/changelog/2026-03-26-new-pull-requests-dashboard-is-in-public-preview
**Category:** Pull Requests

### Summary

A redesigned pull requests dashboard at github.com/pulls is now available as a public preview, featuring a new inbox view that surfaces PRs needing your review, requiring fixes, or ready to merge. Custom saved views allow you to create and organize persistent queries, and an enhanced search bar supports content-assist auto-complete as well as advanced `AND`/`OR`/nested query syntax. The preview can be enabled via the **New Pull Requests Dashboard** toggle in GitHub's feature preview settings.

### Additional Resources

- [Exploring early-access releases with feature preview (GitHub Docs)](https://docs.github.com/en/get-started/using-github/exploring-early-access-releases-with-feature-preview) — Explains how to enable and disable feature previews on GitHub.com, including the new pull requests dashboard.
- [Filtering and searching issues and pull requests (GitHub Docs)](https://docs.github.com/en/issues/tracking-your-work-with-issues/filtering-and-searching-issues-and-pull-requests) — Reference for the search qualifiers available in GitHub PR/issue searches, useful for building saved views.

---

## Security (Dependabot / Code Scanning)

### Credential revocation API now supports GitHub OAuth and GitHub app credentials

**Published:** 2026-03-26
**Source:** https://github.blog/changelog/2026-03-26-credential-revocation-api-now-supports-github-oauth-and-github-app-credentials
**Category:** Security (Dependabot / Code Scanning)

### Summary

The credential revocation API has been extended to cover OAuth app tokens, GitHub App user-to-server tokens, and GitHub App refresh tokens, in addition to the previously supported classic and fine-grained personal access tokens. The unauthenticated API allows anyone to submit a bulk revocation request for up to 1,000 exposed tokens per request, automatically revoking them, logging the revocation, removing any organization access, and notifying the token owner by email. The API is rate-limited to 60 unauthenticated requests per hour to prevent abuse.

### Additional Resources

- [Revoke a list of credentials — REST API (GitHub Docs)](https://docs.github.com/en/rest/credentials/revoke?apiVersion=2022-11-28#revoke-a-list-of-credentials) — API reference including accepted credential types, request format, and HTTP response codes with a `curl` example.
- [Token expiration and revocation (GitHub Docs)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/token-expiration-and-revocation) — Explains all the ways tokens can expire or be revoked, including third-party revocation via the credential revocation API.
- [About secret scanning (GitHub Docs)](https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning) — Overview of how GitHub detects exposed credentials in repositories and notifies owners, which complements the programmatic revocation capability.

---

## Issues

### Agent activity in GitHub Issues and Projects

**Published:** 2026-03-26
**Source:** https://github.blog/changelog/2026-03-26-agent-activity-in-github-issues-and-projects
**Category:** Issues

### Summary

Two new features now surface coding agent activity directly inside planning tools. In GitHub Issues, when a coding agent (Copilot, Claude, Codex, etc.) is assigned to an issue, its live session status — queued, working, waiting for review, or completed — appears under the Assignees sidebar, with a direct link to session logs. In GitHub Projects, agent sessions are now visible in both table and board views, including the current status of each session; enable this via **View > Show agent sessions**. Both features are generally available for all repositories with coding agent access.

### Additional Resources

- [About GitHub Copilot coding agent (GitHub Docs)](https://docs.github.com/en/copilot/concepts/about-copilot-coding-agent) — Explains how the Copilot coding agent works, how sessions are managed, and how agents interact with issues and pull requests.
- [Tracking GitHub Copilot's sessions (GitHub Docs)](https://docs.github.com/en/copilot/how-tos/agents/copilot-coding-agent/tracking-copilots-sessions) — Guide on how to monitor ongoing and completed Copilot coding agent sessions from the agents panel and agents page.
- [GitHub Community discussion — Agent sessions in Projects](https://github.com/orgs/community/discussions/190731) — Community thread for sharing feedback on the agent sessions feature in GitHub Projects.

---

## Others

### Updates to our Privacy Statement and Terms of Service: How we use your data

**Published:** 2026-03-25
**Source:** https://github.blog/changelog/2026-03-25-updates-to-our-privacy-statement-and-terms-of-service-how-we-use-your-data
**Category:** Others

### Summary

GitHub has updated its Privacy Statement and Terms of Service, effective April 24, 2026. The most notable change is that interaction data — including inputs, outputs, code snippets, and context — from Copilot Free, Pro, and Pro+ users will be used to train and improve GitHub's AI models unless users opt out in settings. Copilot Business and Enterprise accounts are unaffected. Additional changes include expanded data-sharing with Microsoft affiliates for AI development, a new dedicated Terms of Service section (Section J) covering AI features and training, and the migration of private-repository access commitments from the Privacy Statement into the Terms of Service.

### Additional Resources

- [GitHub General Privacy Statement (GitHub Docs)](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement) — The full updated Privacy Statement, detailing how GitHub collects, uses, and shares personal data including AI interaction data.
- [GitHub Terms of Service (GitHub Docs)](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service) — The updated Terms of Service, including the new Section J on AI features, training, and user data controls.
- [Copilot privacy settings](https://github.com/settings/copilot) — The settings page where Copilot Free, Pro, and Pro+ users can opt out of having their interaction data used for AI model training.

---
