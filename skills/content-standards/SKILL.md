---
name: content-standards
description: "For \"rewrite the meta descriptions\", \"fix the page titles\", \"add alt text to the images\", \"is this copy any good?\". Content quality and SEO reference for pages: page titles, meta descriptions, slugs, headings, alt text, structure and copy, with the thresholds the site scan applies. Load when writing or reviewing copy, or setting SEO fields."
---

# content-standards

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "content-standards"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "content-standards"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
