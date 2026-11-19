---
name: themespot-hubspot-cms
description: "For \"how do module fields work?\", \"why won't this HubDB page render?\". HubSpot CMS mechanics under ThemeSpot UI: CMS React modules, fields, HubL, HubDB, limits."
---

# themespot-hubspot-cms

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "themespot-hubspot-cms"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "themespot-hubspot-cms"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
