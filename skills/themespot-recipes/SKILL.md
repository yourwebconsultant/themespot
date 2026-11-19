---
name: themespot-recipes
description: "For \"a sticky header\", \"an FAQ\", \"a pricing toggle\", \"a logo cloud\". Proven patterns: video, registration, logos, metrics, FAQ, pricing, menus, headers."
---

# themespot-recipes

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "themespot-recipes"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "themespot-recipes"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
