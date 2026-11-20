# Changelog

## 3.9.0

- The skills name ThemeSpot's MCP server, `themespot`, and its `skill` and `skill_read` tools in words, and each other by plain name, where they named Claude Code's own tool names, so the same skills folder works in any client that loads skills. The `themespot` skill is now ThemeSpot over MCP: signing in is described for any client, and the steps only Claude Code takes are marked as Claude Code's. The agent and its tools are unchanged.

## 3.8.1

- ThemeSpot's word for checking a site, a page or a theme is now QA: the agent's description, this README, the skills, the plans and the tools' descriptions say QA, a QA run and scheduled QA. Only the words changed: the tool that runs QA is still `scan`, with the same actions, fields and answers.

## 3.8.0

- Ask for a new theme and the agent makes it here: `theme_change` action create makes a new React theme on ThemeSpot UI in the site's ThemeSpot workspace, with its brand settings from the site's saved design guidelines when there are some, and binds this connection to it, replacing any binding, so the build carries on in the same conversation instead of starting in the app. It takes the theme's name and what you want of it, works on every plan, and needs the dev role. A connection that uses a key makes the theme and does not bind it. A new HubL theme is still made in the ThemeSpot app, at https://my.themespot.app.

## 3.7.1

- Theme deploys that reach HubSpot: first deploy free, 1 token after. The free one is now the first theme deploy on your account, whichever of your sites it is on, where it was one on every site before.

## 3.7.0

- Theme code through your own agent, this plugin included, is on every plan, and a theme deploy that reaches HubSpot uses 1 token, the first on each site free. A new module in a theme now starts from one of ThemeSpot UI's boilerplates: `theme_change` action create_module takes an `archetype` (content, image, video, form, hubdb, featured-post or island) and writes that boilerplate into the theme, renamed, with its fields, Style group and defaults in place. `check` lists every rule a comment in the theme switched off, with its reason, and says when a theme built before ThemeSpot UI 2.3.0 has its house-rule errors counted as warnings, and how it becomes strict.

## 3.6.0

- The plugin tells ThemeSpot's server that it is the ThemeSpot plugin, so the server's opening facts say that the plugin's skills load their guides from it. ThemeSpot's server now says which guide fits which job, each tool that makes changes names the guide to load before its first change, and a change whose guide ThemeSpot has no record of being loaded says so in its answer, once, and still runs. Binding a theme answers what it is built on and the guide for each kind of change; a new module answers its guide and the module contract's short form.

## 3.5.0

- ThemeSpot UI's own authoring guides are skills here now: `themespot-build-theme`, `themespot-build-from-reference`, `themespot-scaffold-module`, `themespot-scaffold-section`, `themespot-scaffold-template`, `themespot-recipes`, `themespot-hubspot-cms` and `themespot-visual-proof`. Like every skill here, each file holds its name and when to use it, and its text, and any file it lists, load from ThemeSpot's server once you have signed in, so a new theme has the module, section and template contracts before it holds a single file. `create-theme` now builds a new or rebuilt theme on ThemeSpot UI with these guides, and still builds out an existing HubL theme in HubL.

## 3.4.1

- What ThemeSpot's server sends when you connect is now the facts of the connection: the site, your role, its plan, the HubSpot permissions it granted and those it did not, the bound theme and what the web tools may read. The agent's own instructions are no longer sent with them; the plugin's agent loads them from ThemeSpot's server as before. A few tool descriptions no longer tell the agent what to say, and `find` action sql says it queries ThemeSpot's read-only copy of your site.

## 3.4.0

- Each ThemeSpot tool now only reads or only makes changes, never both, and says which, so Claude Code can let the reads run without asking and ask before a change. Reading a theme's code stays `theme`; changing it, binding a theme and reading the theme settings saved in HubSpot (whose first read sets up a hidden draft page there) are `theme_change`. Running a scan stays `scan`; reading scans and their findings is `results`; recording or updating a finding stays `finding`. Reading a web page stays `web`; capturing a page and comparing a draw with that capture are `capture`. Every tool now has a title.

## 3.3.0

- First public release. ThemeSpot for Claude Code is the client for ThemeSpot's hosted MCP server, `https://api.themespot.app/mcp`: you sign in with your ThemeSpot account in the browser, and there is nothing to install. It brings one agent, `themespot`, whose file is short and which loads its full instructions from ThemeSpot's server when it starts, and skills for theme development, website migration and maintenance on a HubSpot website. Each skill's file here holds its name and when to use it; its text, and any file it lists, load from ThemeSpot's server once you have signed in, so they are always the current ones. The plugin holds no reference files and runs nothing of its own on your computer: the README's "What this plugin runs, sends and fetches" says all it does.
