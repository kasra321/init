# Project: init

## Structure

- `local/` — untracked scratch space for local-only files
- `wiki/` — GitHub Wiki (git submodule), editable via Obsidian or any markdown editor

## Wiki Conventions

Wiki pages live in `wiki/` (submodule linked to the GitHub Wiki).

### Frontmatter

All markdown files in `wiki/` must include YAML frontmatter:

```yaml
---
title: Page Title
description: One-liner summary of the page
tags: []
created: "YYYY-MM-DD"
---
```

- **description**: A single sentence summarizing the page
- **tags**: Use existing tags from Obsidian's tag pane before creating new ones
- **created**: Date the page was first created
- Use the template at `wiki/.obsidian/templates/Default Note.md` for new pages

### Obsidian

The `wiki/.obsidian/` folder contains shared vault settings:
- `app.json` — wikilink format, attachment folder (`assets/`)
- `core-plugins.json` — enabled core plugins
- `community-plugins.json` — required community plugins (figma-embed, dataview, juggl)
- `templates/` — note templates

Do not commit `.obsidian/workspace.json` or user-specific settings.

### Pushing Wiki Changes

```bash
git -C wiki add . && git -C wiki commit -m "update wiki" && git -C wiki push
```
