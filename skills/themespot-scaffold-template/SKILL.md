---
name: themespot-scaffold-template
description: "For \"a new page template\", \"a landing page template\". A new page template: annotation, route, sections, the base layout."
---

# themespot-scaffold-template

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "themespot-scaffold-template"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "themespot-scaffold-template"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
