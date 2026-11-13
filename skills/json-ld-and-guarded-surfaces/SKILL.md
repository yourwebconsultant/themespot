---
name: json-ld-and-guarded-surfaces
description: "For \"add schema to this page\", \"why is there duplicate JSON-LD?\", \"set the canonical URL\". JSON-LD, structured data and schema markup on a page — trace a block to its exact source, inspect-first, no duplicates — and the guarded page surfaces, a page's custom head and footer HTML (headHtml, footerHtml), canonical URL (linkRelCanonicalUrl) and attached stylesheets. Load before answering about a page's JSON-LD or structured data, and before touching any of those settings."
---

# json-ld-and-guarded-surfaces

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "json-ld-and-guarded-surfaces"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "json-ld-and-guarded-surfaces"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
