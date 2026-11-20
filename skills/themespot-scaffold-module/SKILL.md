---
name: themespot-scaffold-module
description: "For \"add a new module to the theme\", \"build a pricing table module\". A new React module on ThemeSpot UI: the module contract, fields, islands."
---

# themespot-scaffold-module

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call the `skill` tool of ThemeSpot's MCP server, `themespot`, with `name: "themespot-scaffold-module"`, and follow the instructions it answers as this skill's own. Read a file they list with that server's `skill_read` tool (`skillName: "themespot-scaffold-module"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot` skill has for signing in.
