---
description: Create a new .agent-config.yml file for the Jekyll site
---

# Create Config Workflow

Use this workflow to generate a `.agent-config.yml` file based on the template and existing site configuration.

## Steps

1. **Check existing config** — Verify if `.agent-config.yml` already exists in the repo root.

2. **Read template** — Load the template from `.agent/templates/.agent-config.yml`.

3. **Detect Jekyll config** — Read `docs/_config.yml` to extract site information.

4. **Populate fields** — Fill in the template with detected values.

5. **Write config file** — Save the new `.agent-config.yml` to the repo root.

6. **Commit if desired** — Optionally stage and commit the new config file.