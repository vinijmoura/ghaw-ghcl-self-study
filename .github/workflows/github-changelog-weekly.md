---
description: Weekly GitHub Changelog Documentation Generator - collects GitHub changelog entries every Sunday, enriches them with additional learning resources, and commits structured Markdown documentation to the repository.
on:
  schedule: weekly on sunday
permissions:
  contents: read
tools:
  web-fetch:
  edit:
network:
  allowed:
    - "github.blog"
    - "*.github.blog"
    - github
    - "docs.github.com"
safe-outputs:
  create-pull-request:
    title-prefix: "[changelog] "
    labels: [documentation, automated]
    draft: false
    auto-merge: true
    if-no-changes: warn
---

# Weekly GitHub Changelog Documentation Generator

You are an automated documentation agent. Your task is to collect the GitHub Changelog entries published during the past week, enrich each entry with additional learning resources, and commit a structured Markdown report to this repository.

## Step 1: Determine the Date Range

Calculate the date range for this week's report:
- **Start date**: The last Sunday (inclusive), at 00:00:00 UTC
- **End date**: The following Saturday (inclusive), at 23:59:59 UTC

This means: any changelog entry published on or after the last Sunday (00:00:00 UTC) and on or before the following Saturday (23:59:59 UTC) should be included.

Use today's date to determine the last Sunday and the following Saturday. The target directory will be:

```
docs/github-changelog/YYYY-WeekN/
```

Where `YYYY` is the 4-digit year and `N` is the ISO week number (no leading zero). For example, if today is 2026-03-15 (week 11), the directory is:

```
docs/github-changelog/2026-Week11/
```

## Step 2: Fetch the GitHub Changelog

Fetch the GitHub Changelog RSS feed to get structured data about all recent posts:

```
https://github.blog/changelog/feed/
```

Parse the RSS XML response and collect all `<item>` entries whose `<pubDate>` falls within the date range calculated in Step 1 (from previous Sunday to today, inclusive).

For each matching item extract:
- **Title** (`<title>`)
- **Publication date** (`<pubDate>`, converted to YYYY-MM-DD format)
- **Description** (the content of `<description>` or `<content:encoded>`, stripping HTML tags to get plain text)
- **Link** (`<link>`)

If the RSS feed is unavailable or returns no entries for the week, fetch the main changelog page:

```
https://github.blog/changelog/
```

and extract entries from the HTML.

## Step 3: Enrich Each Entry with Additional Resources

For each changelog entry collected in Step 2, use web-fetch to look up additional learning resources. For each entry's title or feature keyword, fetch relevant pages from:

1. **Official GitHub documentation** — search `https://docs.github.com` for pages that explain the feature (e.g., fetch `https://docs.github.com/search?query=<feature-name>` or directly known documentation paths)
2. **GitHub blog** — fetch `https://github.blog/?s=<feature-name>` or known related blog posts
3. **Example GitHub repositories** — use the GitHub search URL `https://github.com/search?q=<feature-name>&type=repositories` to find repositories demonstrating the feature
4. **Tutorials or technical blog posts** — fetch any related blog posts or tutorials discovered via web-fetch

For each resource found, note:
- The URL
- A short one-sentence summary of what the resource demonstrates or explains

Prioritize official documentation first, then example repos, then blogs/tutorials. Limit to **at most 3 resources per entry** to keep the report concise and avoid excessive network requests. If the RSS feed contains more than 10 entries for the week, only enrich the 10 most recently published entries.

## Step 4: Create the Documentation File

Create the following Markdown file in the repository using the `edit` tool:

```
docs/github-changelog/YYYY-WeekN/changelog.md
```

The file must have this structure:

```markdown
# GitHub Changelog — Week N, YYYY

> **Period:** YYYY-MM-DD to YYYY-MM-DD
> **Source:** https://github.blog/changelog/

---

## GitHub Actions (CI/CD)

### Feature Title 1

**Published:** YYYY-MM-DD
**Source:** https://github.blog/changelog/...
**Category:** <one category from the preferred order above>

### Summary

2-4 sentence summary of the changelog update in plain language, preserving the key behavior change, impacted users, and rollout/status notes if available.

### Additional Resources

- [Resource title](URL) — Short explanation of what this resource demonstrates.
- [Resource title](URL) — Short explanation of what this resource demonstrates.

---

### Feature Title 2

...
```

Rules for the content:
- Use category section headings (`##`) for each category that has at least one item.
- Use feature headings as `###` inside each category section.
- The category section order must be exactly:
  1. GitHub Actions (CI/CD)
  2. GitHub Copilot (AI)
  3. Code Versioning (Repositories + Git)
  4. Pull Requests
  5. Security (Dependabot / Code Scanning)
  6. Codespaces
  7. Packages / Releases
  8. GitHub Pages
  9. Issues
  10. Social Features (Stars, Forks, Watch)
  11. Others (only when needed)
- Omit empty category sections.
- Use the exact title from the changelog as the feature heading (`###`).
- Include the publication date in `YYYY-MM-DD` format.
- Include the direct link to the original changelog post.
- Do not include the full original description.
- Create a concise summary for each item (2-4 sentences) based on the changelog description (HTML stripped).
- Add a `Category` field for every item using exactly one category from the preferred order list.
- Group items by category and present categories following the preferred order.
- Within each category, sort items by publication date descending (newest first).
- List all additional resources found, with a short one-sentence explanation for each.
- If no changelog entries were found for the week, write a short note indicating there were no updates published for this period.
- Separate each entry with a `---` horizontal rule.

## Step 5: Create a Pull Request

After creating the file, use the `create-pull-request` safe output to propose a pull request with the new documentation file. The pull request title should describe the week (e.g., "Weekly GitHub changelog digest — 2026-Week11").
