---
name: themespot-visual-proof
description: "For \"does it match the design?\", \"compare it on mobile\". Drawing a ThemeSpot UI theme and comparing it with a reference at desktop and mobile."
---

# themespot-visual-proof

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call the `skill` tool of ThemeSpot's MCP server, `themespot`, with `name: "themespot-visual-proof"`, and follow the instructions it answers as this skill's own. Read a file they list with that server's `skill_read` tool (`skillName: "themespot-visual-proof"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot` skill has for signing in.
