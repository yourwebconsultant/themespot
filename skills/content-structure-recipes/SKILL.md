---
name: content-structure-recipes
description: "For \"add a section to this page\", \"move the testimonials up\", \"add a field to the contact form\". Worked examples and field shapes for edit action structure (library sections, widths, section styles, moves), edit action page (field targeting, pageRef links, repeaters, clearing, the stale-write hash, page settings) and go_live action form_create / go_live action form_edit. Load when one of those calls needs more than its description gives."
---

# content-structure-recipes

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "content-structure-recipes"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "content-structure-recipes"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
