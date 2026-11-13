---
name: create-theme
description: "For \"build a theme from this design\" and \"build out the new theme\", once that theme exists in ThemeSpot and this connection is bound to it. Building out a newly provisioned HubL theme you are bound to: read the design guidelines, ask two questions in one message, then tokens, theme.json, layouts, sections, templates, modules last; check every batch, seed links from the portal, and promote only with approval. Load when asked to build out the theme you are bound to."
---

# create-theme

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "create-theme"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "create-theme"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
