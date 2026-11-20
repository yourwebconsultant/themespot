---
name: themespot
description: "ThemeSpot over MCP: \"what is ThemeSpot?\", \"how is this better than HubSpot's own MCP?\", \"which site am I on?\", \"sign in to another site\", \"edit the theme on my machine\", \"what will this cost?\". What ThemeSpot is (the content mirror, the HubL renderer, ThemeSpot UI and QA), signing in, which site a connection is on, team access, the user's role and plan, where each skill's text and the agent's instructions come from, working on a theme from your own disk (pull, edit, push), seeing a page, and how tokens are charged. Load with hubspot-websites, the root skill, whenever a task touches a ThemeSpot site."
---

# ThemeSpot over MCP

ThemeSpot gives your agent the tools and context to build, migrate and maintain a HubSpot website: theme development on ThemeSpot UI, website migration, and ongoing maintenance. It works through ThemeSpot's hosted MCP server, `themespot`, at `https://api.themespot.app/mcp`, and needs a ThemeSpot account (free) with the HubSpot website connected, at https://my.themespot.app.

## Signing in

1. The client connects the `themespot` server at that address and asks the user to sign in. The browser opens ThemeSpot.
2. The user signs in, chooses the site this connection works on, and allows access.

**In Claude Code:** the ThemeSpot plugin connects the server. `/mcp`, select `themespot`, and choose **Authenticate**. Claude Code keeps the sign-in; the plugin stores nothing.

Until they have signed in, no ThemeSpot tool is listed: say so and give these steps rather than guessing at a site.

## The rest of this skill

Once signed in, load the rest before you act on this skill: call the `skill` tool of ThemeSpot's MCP server, `themespot`, with `name: "themespot"`, and follow what it answers as this skill's own. It holds team access, first use, plans, tokens, the agent, working from your own disk and seeing a page.

## Links

- The ThemeSpot app: https://my.themespot.app
- Documentation: https://themespot.app/docs
- Help: https://themespot.app/docs/support
- Privacy: https://themespot.app/privacy
- Terms: https://themespot.app/terms
