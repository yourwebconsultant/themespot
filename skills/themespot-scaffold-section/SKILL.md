---
name: themespot-scaffold-section
description: "For \"add a new section\", \"a new band for the home page\". A new drag-and-drop section: module composition, the spacing contract, fallbacks."
---

# themespot-scaffold-section

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "themespot-scaffold-section"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "themespot-scaffold-section"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
