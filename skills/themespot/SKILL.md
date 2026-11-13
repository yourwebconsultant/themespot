---
name: themespot
description: "ThemeSpot from Claude Code: \"what is ThemeSpot?\", \"how is this better than HubSpot's own MCP?\", \"which site am I on?\", \"sign in to another site\", \"edit the theme on my machine\", \"what will this cost?\". What ThemeSpot is (the content mirror, the HubL renderer, ThemeSpot UI and QA), signing in, which site a connection is on, team access, the user's role and plan, the plugin's agent and where its instructions come from, working on a theme from your own disk (pull, edit, push), seeing a page, and how tokens are charged. Load with hubspot-websites, the root skill, whenever a task touches a ThemeSpot site."
---

# ThemeSpot from Claude Code

ThemeSpot gives Claude the tools and context to build, migrate and maintain a HubSpot website: theme development on ThemeSpot UI, website migration, and ongoing maintenance. This plugin is the client for ThemeSpot's hosted MCP server, `themespot`. It needs a ThemeSpot account (free) with the HubSpot website connected, at https://my.themespot.app.

## Signing in

1. `/mcp`, select `themespot`, and choose **Authenticate**. The browser opens ThemeSpot.
2. The user signs in, chooses the site this connection works on, and allows access.

Until they have signed in, no ThemeSpot tool is listed: say so and give these steps rather than guessing at a site. Claude Code keeps the sign-in; the plugin stores nothing.

## The rest of this skill

Once signed in, load the rest before you act on this skill: call `mcp__plugin_themespot_themespot__skill` with `name: "themespot"`, and follow what it answers as this skill's own. It holds team access, first use, one site per connection, plans, tokens, the agent, working from your own disk and seeing a page.

## Links

- The ThemeSpot app: https://my.themespot.app
- Documentation: https://themespot.app/docs
- Help: https://themespot.app/docs/support
- Privacy: https://themespot.app/privacy
- Terms: https://themespot.app/terms
