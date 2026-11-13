---
name: theme-settings-and-tokens
description: "For \"change our brand colour\", \"why is my heading in Arial?\", \"the font doesn't match\". Design tokens and theme settings: a theme's brand colours, fonts and spacing are defaults in its fields, the site's saved theme settings override them, and the brand kit can sit under both. How to change the brand in one place, read what is really saved, and say which value shows. Load before changing a colour, a font, spacing or any theme field."
---

# theme-settings-and-tokens

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "theme-settings-and-tokens"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "theme-settings-and-tokens"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
