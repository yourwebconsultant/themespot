---
name: fix-visual-defect
description: "For \"fix the hero gap\", \"there's a stray line under the header\", \"the buttons overlap on my phone\". Fixing something on a page that looks wrong — a stray line or border, a gap, an overlap, something misaligned, 'it shouldn't do that': ask where it was seen, reproduce it at that screen, name the cause in source, then one edit and one check. Load before you edit to fix or remove a visual defect."
---

# fix-visual-defect

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "fix-visual-defect"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "fix-visual-defect"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
