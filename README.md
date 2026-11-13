# ThemeSpot for Claude Code

ThemeSpot gives Claude the tools and context to build, migrate and maintain a HubSpot website: theme development on ThemeSpot UI, website migration, and ongoing maintenance, through ThemeSpot's hosted MCP server. It works alongside HubSpot's own connector. Your own Claude model does the thinking; ThemeSpot does the work on your HubSpot site, with the same tools, instructions and checks as the agent in the ThemeSpot app at https://my.themespot.app.

This plugin is the client for ThemeSpot's MCP server, and it needs a ThemeSpot account (free) with your HubSpot website connected, at https://my.themespot.app. There is nothing to install and no key to paste into a config file: you sign in with your ThemeSpot account in the browser. The plugin holds the server's address, one short agent and each skill's name and when to use it; the agent's instructions and the skills' text load from ThemeSpot's server once you have signed in.

What is sent to ThemeSpot: each tool call Claude makes, with what it carries (a page's id, the text of an edit, a theme's files), goes to `https://api.themespot.app`, which reads and changes your HubSpot website on your behalf, within the role you hold on it and the access you allowed when you signed in. [What this plugin runs, sends and fetches](#what-this-plugin-runs-sends-and-fetches) says it all, with ThemeSpot's privacy policy and terms.

## Before you start

- A ThemeSpot account, with your HubSpot website connected: sign up and connect HubSpot at https://my.themespot.app.
- Claude Code.

## Install

```sh
claude plugin marketplace add yourwebconsultant/themespot
claude plugin install themespot@themespot
```

Or, inside a Claude Code session: `/plugin marketplace add yourwebconsultant/themespot`, then `/plugin install themespot@themespot`. On Claude Code 2.1.275 or later that is one step: `/plugin install themespot --marketplace yourwebconsultant/themespot`.

## Connect

1. In Claude Code, run `/mcp`, select `themespot` (listed as `plugin:themespot:themespot`) and choose **Authenticate**.
2. Your browser opens ThemeSpot. Sign in, choose the website this connection works on, and allow access.
3. Back in Claude Code, the ThemeSpot tools are listed. Ask "which site am I on?" to check.

One connection works on one website. To switch, run `/mcp`, select `themespot`, clear its authentication, and sign in again choosing the other website. You can see and revoke the apps connected to your account at https://my.themespot.app/settings/connect-your-ai#connected-ai-clients.

Claude Code finds how to sign in from the server itself (OAuth 2.1 with PKCE; Claude Code registers itself as a client), and keeps the sign-in in its own credential store. The plugin holds no credential.

## What is inside

- **The `themespot` MCP server**: `https://api.themespot.app/mcp`. Its tools are named `mcp__plugin_themespot_themespot__<tool>` in Claude Code.
- **One agent**, which Claude uses when a task fits or you ask ("use the themespot agent to …"):

| Agent | What it does |
|---|---|
| `themespot` | ThemeSpot's agent for a HubSpot website, through ThemeSpot's hosted MCP server: pages and blog posts, their structure and copy, redirects, forms, files and images, bulk edits, scans and findings, and reading any theme's code; with a theme bound (dev role, Starter plan or above), changing it: templates, sections, modules, CSS and design tokens, with a check on every batch, renders and the deploy request. Drafts and live changes run when called, Claude Code's own permission prompt the gate; only a theme deploy waits for the owner in ThemeSpot. It loads its full instructions from ThemeSpot's server when it starts. |

  Its file is short: when it starts, it loads its full instructions from ThemeSpot's server, so they are always the current ones, and it does what your role on the site allows.
- **Skills**, which load when a task needs them: `themespot`, `content-standards`, `content-structure-recipes`, `create-page`, `create-standalone-module`, `create-theme`, `fix-visual-defect`, `hubl-authoring`, `hubspot-truth`, `hubspot-websites`, `json-ld-and-guarded-surfaces`, `theme-settings-and-tokens`, `themes` and `themespot-ui`. Each file here holds the skill's name and when to use it; its text, and any file it lists, load from ThemeSpot's server when it is used, once you have signed in, so they are always the current ones. The `themespot` skill also says what ThemeSpot is and how to sign in, before you have.

## Using it

Ask for what you want in plain words: "rewrite the meta descriptions on our service pages", "the hero on the pricing page has a gap under the heading on mobile, fix it", "match this design" with an image. Drafts and live changes run when Claude calls the tool, through Claude Code's own permission prompt; a theme deploy waits for an approval in ThemeSpot (below).

With a theme bound for code changes, you can also ask Claude to edit the theme on your machine: it copies the theme's files into a folder, edits them there with its own tools, and sends the changes back to ThemeSpot as one saved version. ThemeSpot checks, previews and deploys only what has been sent back, so nothing in the folder counts until then.

## What each plan includes

Site management is free on every plan, and so is theme code in the ThemeSpot app at https://my.themespot.app. Theme code through your own agent, this plugin included, needs Starter.

**Free:** one site, and full site management: find, read and edit pages, blog posts, forms, redirects, files and images as drafts, put them live, render, walk and check theme files, see what a change reaches, and the change history. Theme code in the ThemeSpot app at https://my.themespot.app: change a theme, create a new one or a standalone module with ThemeSpot UI, preview it and deploy it. Up to 500 pages kept in sync. Scans you run yourself, from a starting token balance that does not refresh; the first page scanned is free. No theme code through this plugin.

**Starter:** one site, and theme code through your own agent, new or existing: binding a theme with `theme_change` action bind, the tools that write theme files, pulling a theme to your disk and pushing it back, preview and the deploy request, and ThemeSpot UI for themes and standalone modules. Every page kept in sync. A monthly token allowance that refreshes, with top-ups on top.

**Pro:** up to three sites, scheduled background scans, eyes walkthroughs, team roles and longer change history. A larger monthly allowance.

**Agency:** any number of sites, audit export and the largest monthly allowance. Plans: https://themespot.app/pricing.

A tool action a plan gates is listed with that plan at the end of its description, as "(Starter plan)". Below it, it answers that it needs that plan, with a link to upgrade; `site` action overview says the plan, what is left of the allowance and what each plan adds, before anything is tried.

## Tokens

Tokens are spent only where ThemeSpot spends on a model or a browser: a scan (by page, or by template or theme), investigating a finding, capturing a web page, comparing a draw with a capture, a fix ThemeSpot runs for you (charged only when it verifies; a fix whose size is uncertain shows an estimate first), and the agent and walkthroughs that run in the ThemeSpot app at https://my.themespot.app. Reads, drafts, going live, deploys, renders, walk, check, impact and approvals are never charged, and nor is anything you fix with your own Claude through this plugin. Something that fails costs nothing. A tool that would cost more than your balance stops before it runs, says the tokens it needs and your balance, and links to a top-up.

## Approvals

Claude Code's own permission prompt is the gate. Drafts and live changes run when Claude calls the tool: page and post drafts, new pages, structure changes, theme files, and publishing a page or post, redirects, forms, blog authors and tags. Every live change is recorded with who made it, from which client and when. Theme deploys are the exception, and the only change that waits for the owner in ThemeSpot: `ship` files a deploy request and answers at once with a link to approve it in ThemeSpot, by you or someone on the site whose role covers it. Claude cannot approve its own request. Once it is approved, ThemeSpot deploys it, and Claude reads the outcome with `history` without waiting.

## Also in Claude.ai and ChatGPT

The same server works as a connector, with the same sign-in:

- **Claude.ai**: Settings, then Connectors, then **Add custom connector**. Name it ThemeSpot, enter `https://api.themespot.app/mcp`, choose **Add**, then **Connect** and sign in.
- **ChatGPT**: Settings, then Apps, then Advanced, and turn on Developer mode. Choose **Create app**, enter `https://api.themespot.app/mcp` with OAuth authentication, then sign in.

There, the server's own instructions and skills stand in for this plugin's agent, and the skill `themespot-agent` holds its instructions whole.

## What this plugin runs, sends and fetches

- **Runs:** nothing of its own on your computer. The plugin has no scripts, hooks, binaries or bundled code, stores nothing, and does not change Claude Code's settings or permissions. Its agent may ask Claude Code's shell, which asks you before each command, to take a headless-browser screenshot of a preview link with Playwright, which may be downloaded from the npm registry the first time, and to save the picture in your working folder; and, when you work on a theme from your own disk, to download the theme's archive from ThemeSpot, unpack it, and pack and upload your changes. When Claude in Chrome is connected, the agent may open a preview link there.
- **Connects:** to one remote MCP server, `https://api.themespot.app/mcp`, over HTTPS. You sign in with OAuth in your browser; Claude Code keeps the sign-in in its own credential store, and the plugin holds no credential.
- **Sends:** the arguments of the tool calls Claude makes, to ThemeSpot, which reads and writes the connected HubSpot website on your behalf, within the role you hold on it and the access you allowed when you signed in. When you work on a theme from your own disk, the folder is uploaded to ThemeSpot as one archive when Claude sends the changes back; ThemeSpot keeps only the files that changed.
- **Fetches:** the agent's full instructions and the text of each skill, from ThemeSpot's server when they are used (the `skill`, `skill_read` and `skill_search` tools), so they are always current. The files in this repository hold only each skill's name and description with a short note on loading its text (the `themespot` skill also says what ThemeSpot is and how to sign in), and a short agent file that says to load its instructions. A screenshot opens the preview link ThemeSpot gave, and the first one may download Playwright from the npm registry; a theme worked on from your own disk is downloaded from ThemeSpot as one archive.

ThemeSpot's privacy policy: https://themespot.app/privacy. Terms: https://themespot.app/terms.

## Support

Help and contact: https://themespot.app/docs/support. Documentation: https://themespot.app/docs. To report a security problem, see [SECURITY.md](SECURITY.md).

## Licence

The plugin's files are licensed by Your Web Consultant under the Apache License, Version 2.0: see [LICENSE](LICENSE) and [NOTICE](NOTICE). The ThemeSpot service they connect to is governed by its own terms, and so is what it sends: the agent's full instructions and the skill text it loads from the server are not among the plugin's files.
