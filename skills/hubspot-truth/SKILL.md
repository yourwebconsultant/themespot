---
name: hubspot-truth
description: "For \"is this live?\", \"why can't I see my change?\", \"which pages will this change reach?\". HubSpot CMS platform reference: drafts and publishing, the page lifecycle (staged, archived, deleted), dynamic pages and where repeating content lives, the two inheritance mechanisms, always-live surfaces, value precedence, translations and revisions. Load when a decision turns on what is draft or live, which pages an edit reaches, or where a type of content should live."
---

# hubspot-truth

ThemeSpot's MCP server holds this skill's text, so it is always the current one. Load it before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "hubspot-truth"`, and follow the instructions it answers as this skill's own. Read a file they list with `mcp__plugin_themespot_themespot__skill_read` (`skillName: "hubspot-truth"`) when a step needs it. Until the user has signed in to ThemeSpot those tools are not listed: say so, and give the steps the `themespot:themespot` skill has for signing in.
