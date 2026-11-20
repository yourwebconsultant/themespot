---
name: themespot-build-theme
description: "For \"build a new theme\", \"rebuild our theme\", \"make this in ThemeSpot UI\". A new or rebuilt theme on ThemeSpot UI, whole: design system, modules, sections, templates, proof."
---

# themespot-build-theme

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call the `skill` tool of ThemeSpot's MCP server, `themespot`, with `name: "themespot-build-theme"`, and follow the instructions it answers as this skill's own. Read a file they list with that server's `skill_read` tool (`skillName: "themespot-build-theme"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot` skill has for signing in.
