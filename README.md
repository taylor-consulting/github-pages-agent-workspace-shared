# GitHub Pages Agent Workspace

This repository contains skills and workflows for managing a Jekyll-based GitHub Pages site using AI agents (e.g., GitHub Copilot).

## Installation

Add this repository as a submodule to your Jekyll site's Git repository:

```bash
git submodule add https://github.com/taylor-consulting/github-pages-agent-workspace-shared .agent
```

## Configuration

Create a `.agent-config.yml` file in the root of your parent Git repository (not in this submodule). Use the template from `templates/.agent-config.yml` as a starting point.

The `.agent-config.yml` file should contain site-specific settings such as:

- Site name, URL, author
- Blog and pages directories
- Git and GitHub configuration

## Usage

The skills in the `skills/` directory provide instructions for AI agents to perform various tasks on your Jekyll site, such as adding blog posts, pages, creating pull requests, and previewing the site.

The workflows in the `workflows/` directory outline step-by-step processes for these tasks.

## Creating a New .agent-config.yml

Use the skill in `skills/create-config/SKILL.md` to generate a new `.agent-config.yml` based on the template and any existing Jekyll site configuration found in your repository.