# GitHub Changelog — Week 11, 2026

> **Period:** 2026-03-04 to 2026-03-11
> **Source:** https://github.blog/changelog/

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

This feature is available on all [plans that include Copilot code review](https://docs.github.com/copilot/concepts/agents/code-review#availability). [Install or upgrade](https://github.com/cli/cli?tab=readme-ov-file#installation) to GitHub CLI [v2.88.0](https://github.com/cli/cli/releases/tag/v2.88.0) or later to get started.

For more details, check out [the GitHub CLI release notes](https://github.com/cli/cli/releases). To learn more about Copilot code review, visit the [Copilot code review documentation](https://docs.github.com/copilot/using-github-copilot/code-review/using-copilot-code-review).

Have feedback or run into an issue? [Open an issue in the cli/cli repository](https://github.com/cli/cli/issues).

### Additional Resources

- [Using Copilot Code Review](https://docs.github.com/en/copilot/using-github-copilot/code-review/using-copilot-code-review) — Official documentation on how to request code review from GitHub Copilot in pull requests, covering both web and CLI workflows.
- [GitHub CLI v2.88.0 release notes](https://github.com/cli/cli/releases/tag/v2.88.0) — Release notes for the CLI version that introduced Copilot as a reviewer option in `gh pr create` and `gh pr edit`.
- [Copilot code review availability](https://docs.github.com/en/copilot/concepts/agents/code-review#availability) — Overview of which Copilot plans include code review capabilities and how to enable the feature.

---

## Major agentic capabilities improvements in GitHub Copilot for JetBrains IDEs

**Published:** 2026-03-11
**Source:** https://github.blog/changelog/2026-03-11-major-agentic-capabilities-improvements-in-github-copilot-for-jetbrains-ides

### Description

This update brings several new features and improvements to GitHub Copilot in JetBrains IDEs. Core agentic capabilities, including custom agents, sub-agents, and plan agent, are now generally available, with agent hooks in preview and auto-approve support for MCP.

It also expands support for agent instruction files, makes auto model selection generally available, enhances the model and reasoning experience, and includes additional user experience and quality improvements.

**New features**

*Agentic capabilities*

- **Custom agents, sub-agents, and plan agent now generally available:** These capabilities make it easier to tailor Copilot to your workflows and collaborate with specialized agents directly within your IDE. Learn more about [creating a custom agent in JetBrains IDEs](https://docs.github.com/copilot/how-tos/use-copilot-agents/coding-agent/create-custom-agents#creating-a-custom-agent-profile-in-jetbrains-ides).
- **Agent hooks support in public preview:** Agent hooks let you run custom commands at key points during agent sessions. You can define your `hooks.json` file in the `.github/hooks/` folder. Supported events include `userPromptSubmitted`, `preToolUse`, `postToolUse`, and `errorOccurred`.
- **Auto-approve support for MCP:** Configure auto-approve for MCP at both the server and tool level via **Settings > GitHub Copilot > Chat > MCP Server and Tool Auto-approve Configuration**.

*Customization and instructions*

- **Agent instruction file support:** Support for `AGENTS.md` and `CLAUDE.md` instruction files, including the ability to generate an initial `AGENTS.md` file.
- **`/memory` slash command:** Quickly open settings for agent instruction files.

*Model selection and reasoning visibility*

- **Auto model selection now generally available:** Copilot can choose a model on your behalf based on real-time model availability and performance.
- **Thinking panel for extended-reasoning models:** A dedicated thinking panel for extended-reasoning models such as Codex, with configurable Anthropic thinking budgets.
- **Context window usage indicator:** A new indicator in the chat panel shows how much context is being used during a conversation.

**User experience**

Improved sign-in experience, more responsive chat panel layout, cleaner auto-approve UI, refined NES trigger timing, and improved support for Windows ARM platforms.

**Quality improvements**

Improved stability when reading terminal output, resolved issues with `replace_string_in_file` tool, addressed UI inconsistencies, and reduced visual glitches such as file icon flicker.

**Deprecation**

Edit mode has been marked as deprecated in the chat mode dropdown.

### Additional Resources

- [Creating custom agents in JetBrains IDEs](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/create-custom-agents) — Official documentation on creating and configuring custom agents in JetBrains IDEs with `.agent.md` profile files.
- [Using agent hooks](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/use-hooks) — Official documentation on configuring agent hooks to run custom commands at key lifecycle events during agent sessions.
- [GitHub Copilot plugin for JetBrains](https://plugins.jetbrains.com/plugin/17718-github-copilot--your-ai-pair-programmer/versions) — JetBrains Marketplace page for installing or upgrading to the latest version of the GitHub Copilot plugin.

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

**Try it out**

This feature is now available in public preview. Join the discussion within [GitHub Community](https://github.com/orgs/community/discussions/189235).

### Additional Resources

- [GitHub Copilot on GitHub.com](https://docs.github.com/en/copilot) — The GitHub Copilot documentation hub covering all Copilot features available on GitHub.com.
- [GitHub Community discussion](https://github.com/orgs/community/discussions/189235) — Community discussion thread for the repository exploration feature, where you can share feedback and experiences.
- [Using GitHub Copilot Chat](https://docs.github.com/en/copilot/how-tos/chat/use-github-copilot-chat-in-githubcom) — Official documentation on interacting with Copilot Chat on GitHub.com to explore codebases and ask contextual questions.

---

## Secret scanning pattern updates — March 2026

**Published:** 2026-03-10
**Source:** https://github.blog/changelog/2026-03-10-secret-scanning-pattern-updates-march-2026

### Description

GitHub secret scanning continually updates its detectors, validators, and analyzers. Here's what's new for March 2026.

- **28 new secret detectors** from 15 providers, including Lark, Vercel, Snowflake, and Supabase.
- **39 detectors now have push protection enabled by default**, including Airtable, Databricks, Heroku, PostHog, and Shopify.
- **Validity checks** added for Airtable, DeepSeek, npm, Pinecone, and Sentry tokens.

**Detectors added**

Secret scanning now automatically detects new secret types including Azure Active Directory application IDs and secrets, Baidu AI API keys, Figma SCIM tokens, Flickr API keys, Langchain LangSmith keys, Lark app credentials, Limbar tokens, PostHog OAuth tokens, Proof API keys, Snowflake Postgres credentials, Supabase tokens, Vercel API keys and tokens, Weatherstack API keys, and WSO2 Choreo personal access tokens.

`Partner` secrets are automatically reported to the secret issuer when found in public repositories through the secret scanning partnership program.

`User` secrets generate secret scanning alerts when found in public or private repositories.

**Validators added**

The following secret types now support validity checks: Airtable personal access token, DeepSeek API key, npm access token, Pinecone API key and environment, Sentry personal token.

### Additional Resources

- [About secret scanning](https://docs.github.com/en/code-security/secret-scanning/introduction/about-secret-scanning) — Official documentation explaining how GitHub automatically detects exposed credentials and API keys to prevent unauthorized access.
- [Supported secret scanning patterns](https://docs.github.com/en/code-security/secret-scanning/introduction/supported-secret-scanning-patterns) — Complete list of all supported secret types detected by GitHub secret scanning, updated for the March 2026 additions.
- [About push protection](https://docs.github.com/en/enterprise-cloud@latest/code-security/concepts/secret-security/about-push-protection) — Documentation on how push protection blocks commits containing matching secrets, now enabled by default for 39 additional detector types.

---

## CodeQL 2.24.3 adds Java 26 support and other improvements

**Published:** 2026-03-10
**Source:** https://github.blog/changelog/2026-03-10-codeql-2-24-3-adds-java-26-support-and-other-improvements

### Description

CodeQL is the static analysis engine behind [GitHub code scanning](https://docs.github.com/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql), which finds and remediates security issues in your code. We've recently released [CodeQL 2.24.3](https://codeql.github.com/docs/codeql-overview/codeql-changelog/codeql-cli-2.24.3/), which adds support for Java 26 and includes various improvements that enhance the accuracy of your code scanning results.

**Language and framework support**

*Java/Kotlin*

- CodeQL now supports Java 26.
- Java analysis now selects the Java version based on Maven POM files across all project modules. It also tries to use Java 17 or higher for all Maven projects if possible, for improved build compatibility.

*JavaScript/TypeScript*

- Added support for React components wrapped by `observer` from `mobx-react` and `mobx-react-lite`.

**Query changes**

*Python*

- Added a new full SSRF sanitization barrier from the new AntiSSRF library.
- When a guard such as `isSafe(x)` is defined, it now also automatically handles `isSafe(x) == true` and `isSafe(x) != false`.

*Ruby*

- Now tracks taint flow through `Shellwords.escape` and `Shellwords.shellescape` for all queries except command injection.

*Java/Kotlin*

- Expanded modeling from `javax` packages to also cover `jakarta` packages, which may lead to increased alerts for packages using the `jakarta` namespace.

*Rust*

- Added support for neutral models (`extensible: neutralModel`).

*C/C++*

- Improved the `cpp/leap-year/unchecked-after-arithmetic-year-modification` query to reduce false positives.

*C#*

- C# 14: Added support for the `field` keyword in properties.

Every new version of CodeQL is automatically deployed to users of GitHub code scanning on github.com.

### Additional Resources

- [CodeQL CLI 2.24.3 changelog](https://codeql.github.com/docs/codeql-overview/codeql-changelog/codeql-cli-2.24.3/) — Full release notes for CodeQL 2.24.3 with details on all language support and query improvements.
- [About code scanning with CodeQL](https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql) — Official documentation explaining how CodeQL works as a static analysis engine to find and remediate security vulnerabilities.
- [CodeQL documentation hub](https://codeql.github.com/docs/) — Comprehensive CodeQL documentation covering language support, writing queries, and configuration options.

---

## Dependabot now supports pre-commit hooks

**Published:** 2026-03-10
**Source:** https://github.blog/changelog/2026-03-10-dependabot-now-supports-pre-commit-hooks

### Description

GitHub Dependabot now natively supports automatic dependency updates for [pre-commit](https://pre-commit.com/) hooks. By adding `pre-commit` as a package ecosystem in your `dependabot.yml` configuration, Dependabot will parse your `.pre-commit-config.yaml`, check each hook's repository for new tags or releases, and open pull requests to update the `rev` field. This is all fully integrated into your existing Dependabot workflow.

Supported features include:

- **Tag and SHA-based revisions**: Works with hooks pinned to Git tags (e.g., `v4.5.0`) or commit SHAs.
- **Grouped updates**: Combine multiple hook updates into a single pull request using Dependabot's existing [grouped updates](https://docs.github.com/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file#groups) configuration.
- **Changelog and release notes**: Pull requests include changelogs and release notes from hook repositories so you can review what's changed before merging.
- **YAML formatting preservation**: Updates modify the `rev` value and any inline version comments (e.g., `# frozen:`) to reflect the new version, all while keeping your existing structure intact.
- **Graceful handling of `local` and `meta` repos**: Dependabot automatically skips `local` and `meta` hook definitions that don't require version updates.
- **Multi-host support**: Works with hooks hosted on GitHub, GitLab, Bitbucket, and other Git hosting providers.

To get started, [configure pre-commit support in Dependabot version updates](https://docs.github.com/code-security/dependabot/dependabot-version-updates/configuring-dependabot-version-updates) and join the [conversation in `dependabot-core`](https://github.com/dependabot/dependabot-core/issues/1524).

### Additional Resources

- [Configuring Dependabot version updates](https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuring-dependabot-version-updates) — Official documentation on how to configure Dependabot to automatically update dependencies, including setting up the new `pre-commit` ecosystem in `dependabot.yml`.
- [pre-commit framework](https://pre-commit.com/) — Official site for the pre-commit framework, explaining how to configure hooks in `.pre-commit-config.yaml` that Dependabot will now keep up to date.
- [Dependabot grouped updates configuration](https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file#groups) — Documentation on how to combine multiple pre-commit hook updates into a single pull request using the `groups` option.

---

## Figma MCP server can now generate design layers from VS Code

**Published:** 2026-03-06
**Source:** https://github.blog/changelog/2026-03-06-figma-mcp-server-can-now-generate-design-layers-from-vs-code

### Description

GitHub Copilot users can now connect to the Figma MCP server to both pull design context into code and send rendered UI to Figma as editable frames. Together, these capabilities support a connected workflow: generate code from a design, send your UI back to Figma for iteration, and pull updates back into your codebase. This feature is available today in VS Code and coming soon to Copilot CLI.

**How it works**

Getting started with the Figma MCP server and GitHub Copilot is simple:

1. Install the [Figma MCP server](https://developers.figma.com/docs/figma-mcp-server/remote-server-installation/#vs-code).
2. Connect your Figma account.
3. Use Copilot to pull design context from Figma into code or create editable frames in Figma from your rendered UIs.

**Who can use this feature**

Any developer with a GitHub Copilot subscription can connect to the Figma MCP server. This is available on all Figma seats and plans. Capturing UI to Figma as editable frames requires the remote MCP server.

Learn more about the [Figma MCP server](https://help.figma.com/hc/articles/32132100833559-Guide-to-the-Figma-MCP-server).

### Additional Resources

- [Guide to the Figma MCP server](https://help.figma.com/hc/articles/32132100833559-Guide-to-the-Figma-MCP-server) — Official Figma documentation covering how to install and use the Figma MCP server to bridge designs and code with GitHub Copilot.
- [Figma MCP server installation for VS Code](https://developers.figma.com/docs/figma-mcp-server/remote-server-installation/#vs-code) — Step-by-step developer guide for installing the remote Figma MCP server in Visual Studio Code to enable UI-to-Figma capabilities.
- [GitHub Community announcements](https://github.com/orgs/community/discussions/categories/announcements) — GitHub Community announcements channel where the Figma MCP server feature was discussed and where you can share feedback.

---

## GitHub Copilot in Visual Studio Code v1.110 — February release

**Published:** 2026-03-06
**Source:** https://github.blog/changelog/2026-03-06-github-copilot-in-visual-studio-code-v1-110-february-release

### Description

The Visual Studio Code February 2026 release makes agents practical for longer-running and more complex tasks. This gives you more control over how they run, new ways to extend what they can do, and smarter session management that keeps context intact.

**Program your agents**

- Automate with hooks: Run your code at key agent lifecycle events to enforce policies, auto-lint, or block commands before they execute.
- Fork a conversation: Branch from any checkpoint to explore an alternative path without losing your starting point.
- Auto-approve from chat: Toggle global auto approval with `/autoApprove` or `/yolo` directly in the chat input and pair it with terminal sandboxing to let agents run within boundaries.
- Queue and steer from chat: Send follow-up messages while the agent is working to redirect its approach without waiting for it to finish.

**Extend your agents**

- Agent plugins: Install prepackaged bundles of skills, tools, hooks, and MCP servers from the Extensions view. This is currently available as an `/experimental` feature.
- Use skills as slash commands: Trigger agent skills from chat, including ones contributed by your extensions.
- Agentic browser tools: Let agents drive the integrated browser to navigate, click, screenshot, and verify their own changes. This is currently available as an `/experimental` feature.
- Create customizations from chat: Generate reusable prompts, skills, agents, and hooks directly from a conversation with `/create-*` commands.

In addition, Copilot CLI is now included in VS Code with native support including diff tabs, trusted folder sync, and right-click to send code snippets.

**Give agents the right context**

- Share agent memory: Agents share and store knowledge across the Copilot coding agent, Copilot CLI, and code review so context builds up over time.
- Plan memory: Plans persist across turns and through compaction, so the agent builds on existing work instead of starting over.
- Built-in Explore subagent: Delegates fast, parallelized codebase research to lightweight models so the Plan agent references specific files and code paths.
- Context compaction: Copilot automatically compacts conversation history when the context window fills up. You can now trigger compaction manually with `/compact`.
- Handle large outputs: Large tool output is written to disk instead of stuffed into context, so important details aren't lost during compaction.

Also, long-distance next edit suggestions predict edits anywhere in your file.

**Related VS Code productivity updates**

- Kitty graphics protocol for high-fidelity images in the terminal.
- Redesigned model picker with search, sections, and rich hover details.
- Chat accessibility improvements for screen readers, keyboard navigation, and notification signals.
- AI coauthor attribution for commits with AI-generated code.

### Additional Resources

- [VS Code February 2026 release notes](https://code.visualstudio.com/updates/v1_110) — Detailed official release notes for Visual Studio Code v1.110 covering all agent features, hooks, plugins, and context management improvements.
- [GitHub Copilot agent hooks documentation](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/use-hooks) — Documentation on configuring agent hooks to automate lifecycle events in Copilot agent sessions in VS Code.
- [GitHub Community announcements](https://github.com/orgs/community/discussions/categories/announcements) — Community hub for the VS Code February 2026 release discussion where users share feedback on new features.

---

## GPT-5.4 is generally available in GitHub Copilot

**Published:** 2026-03-05
**Source:** https://github.blog/changelog/2026-03-05-gpt-5-4-is-generally-available-in-github-copilot

### Description

GPT-5.4, OpenAI's latest agentic coding model, is now rolling out in GitHub Copilot. In our early testing of real-world, agentic, and software development capabilities, GPT-5.4 consistently hits new rates of success. It also shows enhanced logical reasoning and task execution for intricate, multi-step, tool-dependent processes.

**Availability in GitHub Copilot**

GPT-5.4 will be available to [Copilot Pro, Pro+, Business, and Enterprise](https://github.com/features/copilot/plans) users.

You'll be able to select the model in the model picker in:

- Visual Studio Code version v1.104.1 and later in all modes: chat, ask, edit, agent
- Visual Studio version 17.14.19 and later in all modes: agent, ask
- JetBrains versions 1.5.66 and later, in all modes: ask, edit, agent
- Xcode versions 0.48.0 and later in all modes: ask, agent
- Eclipse versions 0.15.1 and later in all modes: ask, agent
- github.com
- GitHub Mobile iOS and Android
- GitHub CLI
- GitHub Copilot Coding Agent

**Enabling access**

Copilot Enterprise and Copilot Business plan administrators must enable the GPT-5.4 policy in Copilot settings.

### Additional Resources

- [Supported AI models in GitHub Copilot](https://docs.github.com/en/copilot/reference/ai-models/supported-models) — Official documentation listing all supported AI models in GitHub Copilot, including availability per plan, client, and premium request multipliers.
- [GitHub Copilot plans](https://github.com/features/copilot/plans) — Overview of Copilot Pro, Pro+, Business, and Enterprise plans detailing which models and features are available at each tier.
- [Changing the AI model in Copilot Chat](https://docs.github.com/en/copilot/how-tos/use-ai-models/change-the-chat-model) — Step-by-step instructions for selecting GPT-5.4 and other models in the Copilot model picker across supported IDEs and GitHub.com.

---

## Discover and manage agent activity with new session filters

**Published:** 2026-03-05
**Source:** https://github.blog/changelog/2026-03-05-discover-and-manage-agent-activity-with-new-session-filters

### Description

GitHub [Enterprise AI Controls and agent control plane](https://docs.github.com/copilot/concepts/agents/enterprise-management) now includes additional session filters, making it easier to discover and manage agent activity across your enterprise.

**What's new**

In addition to searching for agentic session activity by agents and by organizations within your enterprise, we've now rolled out the following filters:

- **Status**: Search for sessions by status, such as queued, in progress, completed, failed, idle waiting for user, timed out, and cancelled.
- **Repository**: Search for sessions by the repository where the agent session occurred.
- **User**: Search for sessions by the user who initiated the agent session.

To learn more, see our documentation on [AI controls and the agent control plane](https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-agents/monitor-agentic-activity).

Join the discussion within [GitHub Community](https://github.com/orgs/community/discussions/178247).

### Additional Resources

- [Monitoring agentic activity in GitHub Enterprise](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-agents/monitor-agentic-activity) — Official documentation on using the AI Controls and agent control plane to filter, discover, and manage agent sessions across your enterprise.
- [Enterprise AI Controls concepts](https://docs.github.com/en/copilot/concepts/agents/enterprise-management) — Conceptual overview of GitHub Enterprise AI Controls, covering how the agent control plane enables administrators to govern Copilot agent usage.
- [GitHub Community discussion](https://github.com/orgs/community/discussions/178247) — Community discussion thread for enterprise agent management features where administrators can share feedback and ask questions.

---
