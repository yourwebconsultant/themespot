---
name: themes
description: "For \"change the theme\", \"make the buttons rounder\", \"deploy the theme\", \"match this design\". Changing a theme's code, by its two axes: templates and sections are HubL in every theme, modules are HubL or React, and the deployment route is ThemeSpot's workspace, Design Manager or Developer Projects. The loop on every route (a check on every batch, look, ship), deploy repair, matching a design, and which leaf to load. Load before changing any theme's code."
---

# themes

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "themes"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "themes"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
