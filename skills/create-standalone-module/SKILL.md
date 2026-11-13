---
name: create-standalone-module
description: "For \"build a calculator I can put on any page\", \"a pricing table module for every theme\". Standalone module reference: a React module in the site's module library, placeable on pages of any theme. When to choose one over a theme module, the two questions to ask first, the library layout, build rules, then a preview, check action theme and the deploy request. Load before creating or editing one."
---

# create-standalone-module

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "create-standalone-module"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "create-standalone-module"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
