# Changelog

## 3.3.0

- First public release. ThemeSpot for Claude Code is the client for ThemeSpot's hosted MCP server, `https://api.themespot.app/mcp`: you sign in with your ThemeSpot account in the browser, and there is nothing to install. It brings one agent, `themespot`, whose file is short and which loads its full instructions from ThemeSpot's server when it starts, and skills for theme development, website migration and maintenance on a HubSpot website. Each skill's file here holds its name and when to use it; its text, and any file it lists, load from ThemeSpot's server once you have signed in, so they are always the current ones. The plugin holds no reference files and runs nothing of its own on your computer: the README's "What this plugin runs, sends and fetches" says all it does.
