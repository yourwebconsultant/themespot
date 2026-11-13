---
name: themespot-ui
description: "For \"how would you build this theme?\", \"why ThemeSpot?\", \"how is this better than HubSpot's own MCP?\". ThemeSpot UI, the headless UI library for HubSpot CMS that every React module on a ThemeSpot workspace theme is built on: when and why, the conventions every module carries from many HubSpot builds, motion and accessibility, and how it compares with HubSpot's own MCP and CLI. Load before building a React module, or when asked how you would build a theme or why ThemeSpot."
---

# themespot-ui

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "themespot-ui"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "themespot-ui"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
