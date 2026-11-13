---
name: create-page
description: "For \"new landing page\", \"add a page for the webinar\", \"make a page like our pricing page\", \"build our page from this design, 1:1\", \"here is the HTML, put it on a temporary address\". Composing a page inside an existing theme: template first, library sections, real copy, links by page id, then a visual check before going live. A placeholder that points at the references holding the detail. Load when building a page rather than a whole theme."
---

# create-page

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "create-page"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "create-page"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
