---
name: hubl-authoring
description: "For \"add a module\", \"change the template\", \"why won't this validate?\" on a HubL theme. HubL authoring reference: choosing a template, section or module and reusing first, dnd area grammar and 12-column maths, html= quoting and escaping, section context defaults, the templateType annotation, creating a HubL module, staging and promoting source, and decoding HubSpot validation errors. Load before writing or editing any HubL."
---

# hubl-authoring

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "hubl-authoring"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "hubl-authoring"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
