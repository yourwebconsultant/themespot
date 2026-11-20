---
name: themespot-build-from-reference
description: "For \"build our theme from this design\", \"match this mockup\", \"recreate this site\". A theme built to match a design the user supplied, compared side by side."
---

# themespot-build-from-reference

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call the `skill` tool of ThemeSpot's MCP server, `themespot`, with `name: "themespot-build-from-reference"`, and follow the instructions it answers as this skill's own. Read a file they list with that server's `skill_read` tool (`skillName: "themespot-build-from-reference"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot` skill has for signing in.
