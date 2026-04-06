---
name: Create Config
description: Creates a new .agent-config.yml file based on the template and detected Jekyll site configuration.
---

# Create Config Skill

## Overview

This skill generates a `.agent-config.yml` file in the root of the parent repository by:

1. Starting with the template from `templates/.agent-config.yml`
2. Detecting existing Jekyll configuration from `docs/_config.yml` (or similar)
3. Populating fields with appropriate values

## When to Use

Use this skill when setting up the agent workspace for a new Jekyll site or when the `.agent-config.yml` is missing or needs updating.

## Steps

1. **Check for existing .agent-config.yml** — If it exists, ask the user if they want to overwrite it.

2. **Read Jekyll config** — Look for `_config.yml` in the site source directory (usually `docs/_config.yml`).

3. **Extract values**:
   - `site.name`: From `title` in _config.yml
   - `site.url`: From `url` in _config.yml
   - `site.author`: From `author` in _config.yml
   - `site.timezone`: From `timezone` in _config.yml
   - `blog.posts_dir`: Usually `docs/_posts`
   - `blog.drafts_dir`: Usually `docs/_drafts`
   - `pages.pages_dir`: Usually `docs/_pages`
   - `git.main_branch`: Check current git branch or default to `main`
   - `github.owner`: Extract from git remote URL
   - `github.repo`: Extract from git remote URL

4. **Create the file** — Write the populated `.agent-config.yml` to the parent repository root.

5. **Validate** — Ensure the file is valid YAML and contains all required fields.