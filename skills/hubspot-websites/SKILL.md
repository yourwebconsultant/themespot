---
name: hubspot-websites
description: "For \"fix this page\", \"new landing page\", \"build a new version of our page from this design\", \"build a new theme\", \"change the theme\", \"why is this page slow\", \"is it live?\". The root skill for work on a HubSpot website: theme or content, drafts against live, what a change to a page, template, section, module or global reaches, the tool for each question, the deployment route rule, when HubSpot's own documentation is the answer, and which skill to load next. Load it first, before any other skill."
---

# hubspot-websites

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "hubspot-websites"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "hubspot-websites"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
