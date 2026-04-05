# GitHub Changelog — Week 14, 2026

> **Period:** 2026-03-29 to 2026-04-04
> **Source:** https://github.blog/changelog/

---

## GitHub Actions (CI/CD)

### GitHub Actions: Early April 2026 updates

**Published:** 2026-04-02
**Source:** https://github.blog/changelog/2026-04-02-github-actions-early-april-2026-updates
**Category:** GitHub Actions (CI/CD)

### Summary

GitHub Actions introduces entrypoint and command overrides for service containers, letting you specify `entrypoint` and `command` keys in workflow YAML using Docker Compose-style syntax. OIDC tokens now include repository custom properties as claims (GA), enabling more granular trust policies with cloud providers without enumerating individual repositories. Azure private networking for GitHub-hosted runners gains VNET failover support in public preview, allowing a secondary subnet to keep workflows running during regional outages. Failover can be triggered manually or automatically by GitHub, with audit log and email notifications to admins.

### Additional Resources

- [GitHub Actions workflow syntax reference](https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax) — Full YAML syntax reference for workflows, including service container configuration with `entrypoint` and `command` keys.
- [About security hardening with OpenID Connect](https://docs.github.com/en/actions/concepts/security/openid-connect) — Explains how OIDC tokens eliminate long-lived secrets and enable granular, claim-based cloud access policies.
- [About Azure private networking for GitHub-hosted runners](https://docs.github.com/en/enterprise-cloud@latest/admin/configuring-settings/configuring-private-networking-for-hosted-compute-products/about-azure-private-networking-for-github-hosted-runners-in-your-enterprise) — Covers Azure VNET configuration options, including the new failover subnet feature.

---

## GitHub Copilot (AI)

### Organization runner controls for Copilot cloud agent

**Published:** 2026-04-03
**Source:** https://github.blog/changelog/2026-04-03-organization-runner-controls-for-copilot-cloud-agent
**Category:** GitHub Copilot (AI)

### Summary

Organization admins can now set a default GitHub Actions runner for Copilot cloud agent across all repositories in their organization, replacing the previous per-repository configuration requirement. Admins can also lock the runner setting so individual repositories cannot override the organization default, ensuring consistent guardrails and infrastructure choices. This makes it easier to roll out Copilot cloud agent at scale with large GitHub-hosted runners or self-hosted runners that have access to internal resources.

### Additional Resources

- [Configuring runners for GitHub Copilot cloud agent in your organization](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/configure-runner-for-coding-agent) — Step-by-step guide on setting default runner types and controlling per-repository overrides at the organization level.
- [Customizing the Copilot cloud agent environment](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/customize-the-agent-environment) — Explains how to use `copilot-setup-steps.yml` to define custom runners and environment setup steps at the repository level.
- [About Copilot cloud agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) — Overview of how Copilot cloud agent works, including its ephemeral GitHub Actions-powered development environments.

---

### Organization firewall settings for Copilot cloud agent

**Published:** 2026-04-03
**Source:** https://github.blog/changelog/2026-04-03-organization-firewall-settings-for-copilot-cloud-agent
**Category:** GitHub Copilot (AI)

### Summary

Organization admins can now manage Copilot cloud agent's built-in internet access firewall across all repositories in their organization from a central location. Controls include enabling/disabling the firewall, toggling the recommended allowlist, adding organization-wide custom allowlist entries (e.g., for internal package registries), and restricting whether repository admins can add their own allowlist entries. By default, all settings continue to allow each repository to decide, preserving existing behavior.

### Additional Resources

- [Customizing the agent firewall for Copilot cloud agent](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/customize-the-agent-firewall) — Documents all firewall configuration options, the recommended allowlist contents, and current firewall limitations.
- [Copilot allowlist reference](https://docs.github.com/en/copilot/reference/copilot-allowlist-reference#copilot-coding-agent-recommended-allowlist) — Lists all hosts included in the default recommended allowlist for Copilot cloud agent.
- [About Copilot cloud agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) — Overview of Copilot cloud agent, including its security model and how it accesses internet resources during task execution.

---

### Copilot cloud agent signs its commits

**Published:** 2026-04-03
**Source:** https://github.blog/changelog/2026-04-03-copilot-cloud-agent-signs-its-commits
**Category:** GitHub Copilot (AI)

### Summary

Copilot cloud agent now cryptographically signs every commit it makes, which appear as `Verified` on GitHub. This ensures commits are genuinely from the agent and have not been tampered with. Critically, this allows Copilot cloud agent to operate in repositories that enforce the "Require signed commits" branch protection rule or ruleset — a previous blocker for agent adoption in security-conscious teams.

### Additional Resources

- [About Copilot cloud agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) — Overview of all Copilot cloud agent capabilities and prerequisites.
- [Available rules for rulesets — Require signed commits](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets#require-signed-commits) — Explains the branch ruleset rule that now works with Copilot cloud agent commits.
- [Managing commit signature verification](https://docs.github.com/en/authentication/managing-commit-signature-verification) — Guide on how commit signing and the `Verified` badge work on GitHub.

---

### GPT-5.1 Codex, GPT-5.1-Codex-Max, and GPT-5.1-Codex-Mini deprecated

**Published:** 2026-04-03
**Source:** https://github.blog/changelog/2026-04-03-gpt-5-1-codex-gpt-5-1-codex-max-and-gpt-5-1-codex-mini-deprecated
**Category:** GitHub Copilot (AI)

### Summary

GitHub deprecated GPT-5.1-Codex, GPT-5.1-Codex-Mini, and GPT-5.1-Codex-Max on April 1, 2026, across all Copilot experiences including Chat, inline edits, ask/agent modes, and code completions. The recommended alternative for all three is GPT-5.3-Codex. Copilot Enterprise administrators may need to explicitly enable the replacement model through their organization's Copilot model policies. No action is required to remove the deprecated models from the selector.

### Additional Resources

- [Supported AI models in GitHub Copilot](https://docs.github.com/en/copilot/reference/ai-models/supported-models) — Reference table of current supported models, retirement history, and availability per Copilot plan and client.
- [Changing the AI model for GitHub Copilot Chat](https://docs.github.com/en/copilot/how-tos/use-ai-models/change-the-chat-model) — Instructions for selecting and switching models in supported IDEs and github.com.
- [Managing Copilot policies for your enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) — Explains how Copilot Enterprise admins can enable or restrict specific models through policy settings.

---

### GitHub Copilot in Visual Studio — March update

**Published:** 2026-04-02
**Source:** https://github.blog/changelog/2026-04-02-github-copilot-in-visual-studio-march-update
**Category:** GitHub Copilot (AI)

### Summary

The March 2026 Visual Studio update brings significant Copilot extensibility improvements, including support for custom agents defined as `.agent.md` files and reusable agent skills. A new `find_symbol` tool adds language-aware symbol navigation to agent mode for C++, C#, TypeScript, and other LSP-supported languages. Enterprise MCP governance now enforces organization allowlist policies for MCP servers, and new profiling integrations enable Copilot to analyze test performance and suggest targeted optimizations directly in the IDE.

### Additional Resources

- [Visual Studio March 2026 blog — Build your own custom agents](https://devblogs.microsoft.com/visualstudio/visual-studio-march-update-build-your-own-custom-agents/) — Detailed walkthrough of custom agents, agent skills, the `find_symbol` tool, and all other March 2026 Copilot features in Visual Studio.
- [Visual Studio 2026 release notes](https://learn.microsoft.com/visualstudio/releases/2026/release-notes) — Official release notes listing all changes and new features in the March Visual Studio update.
- [awesome-copilot repository](https://github.com/github/awesome-copilot) — Community-shared Copilot skills, cookbook recipes for the Copilot SDK, and example custom agent definitions.

---

### Copilot SDK in public preview

**Published:** 2026-04-02
**Source:** https://github.blog/changelog/2026-04-02-copilot-sdk-in-public-preview
**Category:** GitHub Copilot (AI)

### Summary

The GitHub Copilot SDK is now in public preview, making the same agent runtime that powers Copilot cloud agent and Copilot CLI available as a programmable SDK. It supports Node.js/TypeScript, Python, Go, .NET, and Java, and provides tool invocation, streaming, file operations, and multi-turn sessions out of the box. Key features include custom tools and agents, fine-grained system prompt customization, blob attachments, OpenTelemetry tracing, a permission framework, and Bring Your Own Key (BYOK) support for OpenAI, Azure AI Foundry, and Anthropic. The SDK is available to all Copilot and non-Copilot subscribers, with prompts counted toward the premium request quota for paid plans.

### Additional Resources

- [github/copilot-sdk — Getting Started Guide](https://github.com/github/copilot-sdk) — Official SDK repository with installation instructions, API reference, and cookbook examples for all five supported languages.
- [awesome-copilot Copilot SDK cookbook](https://github.com/github/awesome-copilot/blob/main/cookbook/copilot-sdk/nodejs/README.md) — Community Node.js cookbook with runnable examples demonstrating how to build custom agents with the SDK.
- [About premium requests in GitHub Copilot](https://docs.github.com/en/copilot/managing-copilot/monitoring-usage-and-entitlements/about-premium-requests) — Explains how SDK prompt usage is counted toward plan quotas and what the multipliers are per model.

---

### Copilot usage metrics now includes per-user GitHub Copilot CLI activity in organization reports

**Published:** 2026-04-02
**Source:** https://github.blog/changelog/2026-04-02-copilot-usage-metrics-now-includes-per-user-github-copilot-cli-activity-in-organization-reports
**Category:** GitHub Copilot (AI)

### Summary

Organization admins can now view per-user CLI activity in both 1-day and 28-day Copilot usage reports, completing coverage after earlier enterprise-level, user-level, and organization-level CLI metrics rollouts. The data includes each user's CLI session counts, request counts, token usage totals, average tokens per request, and last known CLI version. This helps admins identify active CLI users, support cost allocation, and plan upgrade rollouts across the organization.

### Additional Resources

- [Copilot usage metrics REST API](https://docs.github.com/en/enterprise-cloud@latest/rest/copilot/copilot-usage-metrics?apiVersion=2026-03-10) — API reference for querying Copilot usage metrics at the enterprise and organization level, including the CLI-specific fields.
- [GitHub Copilot usage metrics reference](https://docs.github.com/en/enterprise-cloud@latest/copilot/reference/copilot-usage-metrics) — Explains all metrics fields available in usage reports, including the CLI-specific breakdown fields added in this update.
- [GitHub Community discussion — Copilot usage metrics announcements](https://github.com/orgs/community/discussions/categories/announcements) — The GitHub Community space for announcements related to Copilot features, including usage metrics updates.

---

## Security (Dependabot / Code Scanning)

### The Security tab is now Security & quality

**Published:** 2026-04-02
**Source:** https://github.blog/changelog/2026-04-02-the-security-tab-is-now-security-quality
**Category:** Security (Dependabot / Code Scanning)

### Summary

The top-level **Security** tab in repositories, organizations, and enterprises on github.com has been renamed to **Security & quality**, collocating code quality findings alongside security alerts for easier triage. The "Vulnerability alerts" sidebar section is now **Findings**, and a new **Code quality** section shows enablement status. All existing URLs and API endpoints remain unchanged, so bookmarks, scripts, and integrations do not need to be updated. This change is available on github.com only and is not included in GitHub Enterprise Server; it lays the groundwork for the upcoming GitHub Code Quality GA launch.

### Additional Resources

- [GitHub Community discussion — Security & quality tab](https://github.com/orgs/community/discussions/177488) — Official community thread for feedback on the Security & quality navigation rename.
- [About code scanning](https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning) — Overview of code scanning alerts that will now surface in the unified Security & quality view.
- [About Dependabot alerts](https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts) — Explains Dependabot vulnerability alerts, which remain accessible under the renamed Findings sidebar section.

---

## Issues

### Improved search for GitHub Issues is now generally available

**Published:** 2026-04-02
**Source:** https://github.blog/changelog/2026-04-02-improved-search-for-github-issues-is-now-generally-available
**Category:** Issues

### Summary

Semantic and hybrid issue search, first introduced in public preview in January 2026, is now generally available across GitHub Issues. The search indexes issue titles and bodies, enabling natural language queries that return conceptually related results — not just keyword matches — with the desired result appearing in the top three results 75% of the time (up from 66% with traditional search). Hybrid search combines semantic and keyword matching in a single query, and the new capability is now also accessible via the REST and GraphQL APIs using `search_type=semantic` or `search_type=hybrid`. Semantic and hybrid queries are rate-limited to 10 requests per minute.

### Additional Resources

- [REST API search endpoint](https://docs.github.com/en/rest/search/search) — Reference documentation for the `/search/issues` endpoint, including the new `search_type` parameter for semantic and hybrid queries.
- [GraphQL search query](https://docs.github.com/en/graphql/reference/queries#search) — GraphQL reference for the `search` query, now supporting `searchType: SEMANTIC` and `searchType: HYBRID` arguments.
- [GitHub Community discussion — Improved issue search feedback](https://github.com/orgs/community/discussions/190865) — The official feedback thread for the improved Issues search feature.

---
