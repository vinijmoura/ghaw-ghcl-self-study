# GitHub Changelog — Week 11, 2026

> **Period:** 2026-03-08 to 2026-03-15
> **Source:** https://github.blog/changelog/

---

## Optionally skip approval for Copilot coding agent Actions workflows

**Published:** 2026-03-13
**Source:** https://github.blog/changelog/2026-03-13-optionally-skip-approval-for-copilot-coding-agent-actions-workflows

### Description

When Copilot coding agent opens a pull request or pushes changes, Copilot is treated like an outside contributor in an open source project. GitHub Actions workflows do not run until approved by a human with the **Approve and run workflows** button.

This helps protect you from security risks, given that GitHub Actions workflows may have access to tokens, secrets, or repository permissions, depending on your configuration. However, it slows down the feedback loop for validating Copilot's work and finding out if tests pass.

In some repositories, you may want GitHub Actions workflows to run automatically so you can iterate more quickly, despite the risks.

**We've added a new repository setting to allow repository administrators to skip the human approval so workflows run immediately.** By default, as before, we'll require approval from a human before workflows run.

To learn more, see ["Configuring settings for GitHub Copilot coding agent"](https://docs.github.com/copilot/how-tos/use-copilot-agents/coding-agent/configuring-agent-settings) in the GitHub Docs.

### Additional Resources

- [Configuring settings for GitHub Copilot coding agent](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/configuring-agent-settings) — Step-by-step guide for enabling the "skip approval" setting for Copilot coding agent Actions workflow runs in repository settings.
- [About Copilot coding agent](https://docs.github.com/copilot/concepts/agents/coding-agent/about-coding-agent) — Conceptual overview of the Copilot coding agent and the security model behind its GitHub Actions integration.
- [About security hardening with OpenID Connect](https://docs.github.com/en/actions/security-for-github-actions/security-hardening-your-deployments/about-security-hardening-with-openid-connect) — Explains best practices for securing GitHub Actions workflows, relevant when granting automated agents broader permissions.

---

## Self-hosted runner minimum version enforcement paused

**Published:** 2026-03-13
**Source:** https://github.blog/changelog/2026-03-13-self-hosted-runner-minimum-version-enforcement-paused

### Description

We're temporarily pausing GitHub Actions enforcement of the minimum self-hosted runner version requirement (v2.329.0) scheduled to take effect on March 16, 2026. Runners below v2.329.0 can still register and configure during this period.

We'll publish an updated timeline and enforcement plan in the coming weeks. We strongly encourage you to continue upgrading your self-hosted runners to v2.329.0 or later as soon as you can (review the [upgrade documentation](https://docs.github.com/enterprise-cloud@latest/actions/reference/runners/self-hosted-runners#runner-software-updates-on-self-hosted-runners) for detailed guidance).

This doesn't change our long-term direction. We still plan to block older runner versions from registration and configuration. We're taking this time to ensure a smooth transition.

For reference, here are the previous communications on this topic:

- [Self-hosted runner minimum version enforcement extended (February 2026)](https://github.blog/changelog/2026-02-05-github-actions-self-hosted-runner-minimum-version-enforcement-extended/)
- [Better diagnostics for VNET injected runners and required self-hosted runner upgrades (December 2025)](https://github.blog/changelog/2025-12-12-better-diagnostics-for-vnet-injected-runners-and-required-self-hosted-runner-upgrades/)

Learn more in [our documentation about self-hosted runner management](https://docs.github.com/actions/hosting-your-own-runners/managing-self-hosted-runners/about-self-hosted-runners).

### Additional Resources

- [About self-hosted runners](https://docs.github.com/en/actions/hosting-your-own-runners/managing-self-hosted-runners/about-self-hosted-runners) — Overview of self-hosted runner capabilities and guidance on managing runner software updates.
- [Self-hosted runner minimum version enforcement extended (February 2026)](https://github.blog/changelog/2026-02-05-github-actions-self-hosted-runner-minimum-version-enforcement-extended/) — Previous changelog entry explaining the enforcement timeline extension and upgrade requirements.
- [Better diagnostics for VNET injected runners (December 2025)](https://github.blog/changelog/2025-12-12-better-diagnostics-for-vnet-injected-runners-and-required-self-hosted-runner-upgrades/) — Earlier announcement introducing the minimum version requirement and upgrade tooling for VNET-injected runners.

---

## Updates to GitHub Copilot for students

**Published:** 2026-03-13
**Source:** https://github.blog/changelog/2026-03-13-updates-to-github-copilot-for-students

### Description

Starting today, students with GitHub Education benefits are now on the new **GitHub Copilot Student plan**. As part of this transition, we've updated the available model lineup. The new GitHub Copilot Student plan allows us to focus on building a long-term, sustainable Copilot experience tailored for students with continued investment in AI-native learning tools.

Please visit our [Community Discussion](https://gh.io/copilot4edu) for a full breakdown of what's changing.

### Additional Resources

- [GitHub Copilot for students — Community Discussion](https://gh.io/copilot4edu) — Full breakdown of what's changing in the GitHub Copilot Student plan, including updated model availability and benefit details.
- [GitHub Education for Students](https://education.github.com/students) — Overview of all GitHub Education benefits available to verified students, including access to Copilot and developer tools.
- [GitHub Copilot Plans](https://github.com/features/copilot/plans) — Comparison of all available GitHub Copilot subscription plans, including the new Student plan.

---

## REST API version 2026-03-10 is now available

**Published:** 2026-03-12
**Source:** https://github.blog/changelog/2026-03-12-rest-api-version-2026-03-10-is-now-available

### Description

Previously, we [introduced calendar-based versioning](https://github.blog/developer-skills/github/to-infinity-and-beyond-enabling-the-future-of-githubs-rest-api-with-api-versioning/) for our REST API, giving us a path to evolving our API while giving integrators plenty of time and clear guidance for upgrading.

Now, we're releasing calendar version **`2026-03-10`**, the newest version of the GitHub REST API. This is the **first calendar version to include breaking changes**.

**What's in this release**

Version `2026-03-10` introduces a set of breaking changes to the REST API. You can find the full list of changes, along with [upgrade guidance](https://docs.github.com/rest/about-the-rest-api/breaking-changes#upgrading-to-a-new-api-version), in our [breaking changes documentation](https://docs.github.com/rest/about-the-rest-api/breaking-changes?apiVersion=2026-03-10).

As a reminder, non-breaking changes (e.g., new endpoints, optional parameters, additional response fields) continue to be available across all supported API versions.

**What this means for existing integrations**

Version `2022-11-28` will continue to be fully supported for at least 24 months from today, and requests that don't include the `X-GitHub-Api-Version` header will continue to default to `2022-11-28`.

When you're ready to upgrade, update the `X-GitHub-Api-Version` header to `2026-03-10` and verify that your integration works as expected.

Use the version picker in our [API documentation](https://docs.github.com/rest) to view the docs for all available versions.

### Additional Resources

- [Breaking changes in the REST API](https://docs.github.com/en/rest/about-the-rest-api/breaking-changes) — Complete list of breaking changes introduced in version `2026-03-10`, including affected endpoints and migration guidance.
- [API versioning overview](https://docs.github.com/en/rest/overview/api-versions) — Explains GitHub's calendar-based REST API versioning and how to specify the API version in requests using the `X-GitHub-Api-Version` header.
- [GitHub REST API reference](https://docs.github.com/en/rest) — Full reference documentation for all REST API endpoints, with a version picker to view docs for each supported API version.

---

## Copilot auto model selection is generally available in JetBrains IDEs

**Published:** 2026-03-12
**Source:** https://github.blog/changelog/2026-03-12-copilot-auto-model-selection-is-generally-available-in-jetbrains-ides

### Description

GitHub Copilot auto model selection is now generally available in JetBrains IDEs for all Copilot plans. With auto, Copilot chooses a model on your behalf based on real-time model availability and performance.

**How it works**

Auto is dynamic, giving you reliable access to your favorite models while mitigating rate limits. It routes to models like GPT-5.4, GPT-5.3-Codex, Sonnet 4.6, and Haiku 4.5 depending on your plan and policies.

- **Transparency**: See which model was used by hovering over the model response.
- **Stay in control**: Switch between auto and any specific model at any time.
- **Respects your policies**: Auto honors all administrator model settings.

**Premium request use**

Premium request use for auto is billed based on the model it selects. All paid subscribers get a 10% discount on the model multiplier when using auto. For example, when auto uses a model with a 1x multiplier, you'll draw down 0.9 premium requests instead of 1.

**Where we're headed**

Soon, auto will become even more intelligent, gaining enhanced capabilities that allow Copilot to select the most appropriate model for your task, matching the model to the complexity level of your request.

### Additional Resources

- [GitHub Copilot plugin for JetBrains IDEs](https://plugins.jetbrains.com/plugin/17718-github-copilot--your-ai-pair-programmer/versions) — Download or update to the latest version of the GitHub Copilot plugin to use auto model selection in JetBrains IDEs.
- [Copilot model multipliers and billing](https://docs.github.com/copilot/concepts/billing/copilot-requests#model-multipliers) — Explains how premium requests are calculated per model and how the 10% auto discount is applied.
- [Copilot conversations community discussion](https://github.com/orgs/community/discussions/categories/copilot-conversations) — Community forum to share feedback and ask questions about GitHub Copilot features including auto model selection.

---

## Actions OIDC tokens now support repository custom properties

**Published:** 2026-03-12
**Source:** https://github.blog/changelog/2026-03-12-actions-oidc-tokens-now-support-repository-custom-properties

### Description

GitHub Actions OpenID Connect (OIDC) tokens now support repository custom properties as claims. A new settings page is available in public preview, making it easy to configure OIDC token claims directly from your repository, organization, or enterprise settings.

Organization and enterprise admins can select custom properties to include in OIDC tokens. Once a property is added to the claim, every repository with that property value set will automatically include it in its OIDC tokens, prefixed with `repo_property_`. You can use these claims to build attribute-based access control (ABAC) policies in Azure, AWS, GCP, and other cloud providers without modifying individual workflows.

With custom properties in OIDC tokens, you can:

- **Eliminate duplication**: Your governance metadata lives in one place and flows automatically into your cloud policies.
- **Reduce configuration drift**: Policies bind directly to repository attributes, so they stay accurate as your organization evolves.
- **Accelerate onboarding**: New repositories automatically inherit the right access policies based on their properties.
- **Create consistent cross-cloud policies**: Turn your existing GitHub metadata into an actionable control surface for managed identities across AWS, Azure, GCP, and beyond.

To learn more, see [Customizing the OIDC token](https://docs.github.com/actions/security-for-github-actions/security-hardening-your-deployments/about-security-hardening-with-openid-connect#customizing-the-token-claims).

### Additional Resources

- [About security hardening with OpenID Connect](https://docs.github.com/en/actions/security-for-github-actions/security-hardening-your-deployments/about-security-hardening-with-openid-connect) — Comprehensive guide to using OIDC tokens with GitHub Actions for secure, secretless cloud deployments.
- [Customizing the OIDC token claims](https://docs.github.com/actions/security-for-github-actions/security-hardening-your-deployments/about-security-hardening-with-openid-connect#customizing-the-token-claims) — Details on adding custom properties and subject claims to OIDC tokens for use in cloud provider trust policies.
- [Managing custom properties for repositories](https://docs.github.com/en/organizations/managing-organization-settings/managing-custom-properties-for-repositories-in-your-organization) — Explains how to create and manage repository custom properties that can now be embedded in OIDC token claims.

---

## Issue fields: Structured issue metadata is in public preview

**Published:** 2026-03-12
**Source:** https://github.blog/changelog/2026-03-12-issue-fields-structured-issue-metadata-is-in-public-preview

### Description

Issue fields are now available in public preview for select GitHub organizations.

If you've been using labels like `priority/p0` or `severity/high` to track structured data in issues, you know the limitations: no types, no validation, no consistency across repositories, and no way to report on them. Issue fields replace unstructured text in the issue body and label-based workarounds with typed, org-wide metadata that's searchable, reportable, and consistent across every repository.

Out of the box, every organization gets four fields preconfigured and pinned to the right issue types: `Priority`, `Effort`, `Start date`, and `Target date`. Create a bug, and you'll see `Priority` and `Effort` in the sidebar. Create a feature and you get all four.

From there, organization admins can customize everything:

- **Four field types**: Single select, text, number, and date, with up to 25 fields per organization.
- **Pin fields to issue types**: Control which fields show up for bugs, features, tasks, your custom types, or issues without a type.
- **Search and filter**: Find issues by field values across repositories.
- **Projects integration**: Add issue fields as columns in project views to group, filter, and sort.
- **Timeline events**: Track who changed which field and when.
- **Full API support**: REST and GraphQL APIs for field settings and values, plus `field_added` and `field_removed` webhook events for GitHub Actions.

Issue fields is rolling out to a selection of organizations. To request access, comment in the [community discussion](https://github.com/orgs/community/discussions/189141) with your organization name and use case.

### Additional Resources

- [Managing issue fields in an organization](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/managing-issue-fields-in-an-organization) — Official documentation on creating, configuring, and managing custom issue fields at the organization level.
- [Issue fields community discussion](https://github.com/orgs/community/discussions/189141) — Request access to the public preview and provide feedback on issue fields with your use case.
- [About GitHub Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects) — Overview of GitHub Projects, which integrates with issue fields to support grouping and filtering by field values.

---

## Request Copilot code review from GitHub CLI

**Published:** 2026-03-11
**Source:** https://github.blog/changelog/2026-03-11-request-copilot-code-review-from-github-cli

### Description

You can now request a review from GitHub Copilot directly from your terminal using the GitHub CLI. Whether you're editing an existing pull request or creating a new one, Copilot is available as a reviewer option in `gh pr edit` and `gh pr create`. There's no need to switch to the browser.

**How it works**

**Non-interactive:** Add Copilot as a reviewer with `gh pr edit --add-reviewer @copilot`.

**Interactive:** When you select reviewers through the interactive prompts, Copilot appears alongside your teammates.

**Faster reviewer and assignee selection**

This release also introduces a search-based experience for selecting reviewers and assignees. Instead of loading all collaborators and teams upfront, results are now fetched as you type. This dramatically improves performance for large organizations and resolves accessibility issues where screen readers were reading thousands of options aloud.

**Who can use this**

This feature is available on all [plans that include Copilot code review](https://docs.github.com/copilot/concepts/agents/code-review#availability). Install or upgrade to GitHub CLI [v2.88.0](https://github.com/cli/cli/releases/tag/v2.88.0) or later to get started.

### Additional Resources

- [Using Copilot code review](https://docs.github.com/en/copilot/using-github-copilot/code-review/using-copilot-code-review) — Complete guide to requesting and working with Copilot code reviews, including how to apply suggested changes.
- [GitHub CLI v2.88.0 release notes](https://github.com/cli/cli/releases/tag/v2.88.0) — Release notes for the GitHub CLI version that introduces the `--add-reviewer @copilot` flag and the search-based reviewer selection UX.
- [GitHub CLI repository](https://github.com/cli/cli) — Source code, installation instructions, and issue tracker for the GitHub CLI tool.

---

## Major agentic capabilities improvements in GitHub Copilot for JetBrains IDEs

**Published:** 2026-03-11
**Source:** https://github.blog/changelog/2026-03-11-major-agentic-capabilities-improvements-in-github-copilot-for-jetbrains-ides

### Description

This update brings several new features and improvements to GitHub Copilot in JetBrains IDEs. Core agentic capabilities, including custom agents, sub-agents, and plan agent, are now generally available, with agent hooks in preview and auto-approve support for MCP.

**New features**

*Agentic capabilities*

- **Custom agents, sub-agents, and plan agent** are now generally available. These capabilities make it easier to tailor Copilot to your workflows and collaborate with specialized agents directly within your IDE.
- **Agent hooks** are available in public preview. Supported events include `userPromptSubmitted`, `preToolUse`, `postToolUse`, and `errorOccurred`. Define your `hooks.json` file in the `.github/hooks/` folder of your repository.
- **Auto-approve support for MCP**: Configure auto-approve at both the server and tool level, reducing manual approvals in chat.

*Customization and instructions*

- **Agent instruction file support**: Support added for `AGENTS.md` and `CLAUDE.md` instruction files, including the ability to generate an initial `AGENTS.md` file.
- **`/memory` slash command**: Quickly open settings for agent instruction files.

*Model selection and reasoning visibility*

- **Auto model selection** is now generally available in JetBrains IDEs for all Copilot plans.
- **Thinking panel** for extended-reasoning models with configurable Anthropic thinking budgets.
- **Context window usage indicator** in the chat panel.

**User experience improvements**

- Improved sign-in experience with automatic chat panel opening after sign-in.
- More responsive chat panel layout and cleaner context/file attachment handling.
- Improved support for Windows ARM platforms.

**Quality improvements**

- Improved stability when reading terminal output.
- Resolved issues where file updates were not applied correctly by the `replace_string_in_file` tool.
- Addressed UI inconsistencies and reduced visual glitches.

**Deprecation**: Edit mode has been marked as deprecated in the chat mode dropdown.

### Additional Resources

- [Creating custom agents in JetBrains IDEs](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/create-custom-agents) — Guide to creating and configuring specialized agent profiles for use within JetBrains IDEs.
- [Agent hooks documentation](https://docs.github.com/copilot/how-tos/use-copilot-agents/coding-agent/use-hooks) — Documentation on configuring agent hooks to automate and integrate workflows during Copilot agent sessions.
- [GitHub Copilot plugin for JetBrains IDEs](https://plugins.jetbrains.com/plugin/17718-github-copilot--your-ai-pair-programmer/versions) — Install or update the latest Copilot plugin for JetBrains IDEs to access all new agentic capabilities.

---

## Explore a repository using Copilot on the web

**Published:** 2026-03-11
**Source:** https://github.blog/changelog/2026-03-11-explore-a-repository-using-copilot-on-the-web

### Description

We've made it easier to explore a repository's file structure when you chat with Copilot on the web.

**What's changed**

Developers can now ask Copilot to show a file, then browse the file tree alongside file contents. With a deeper view into how files relate to the broader codebase, it's never been easier to jump between files and ask Copilot the right questions in context.

**Seamlessly add references to chat**

As you navigate the file explorer, files you select get automatically added to your current chat as temporary references. You can choose to add these as permanent references by clicking the reference token or double clicking the file preview tab.

This feature is now available in public preview. Join the discussion within [GitHub Community](https://github.com/orgs/community/discussions/189235).

### Additional Resources

- [About GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/about-github-copilot-chat) — Overview of GitHub Copilot Chat capabilities across web, IDEs, and mobile environments.
- [Using Copilot on GitHub.com](https://docs.github.com/en/copilot/how-tos/chat/use-copilot-on-github.com) — Guide to all GitHub Copilot Chat features available directly in the browser, including repository context.
- [Repository exploration community discussion](https://github.com/orgs/community/discussions/189235) — Community forum thread for sharing feedback on the new repository exploration feature in Copilot on the web.

---
