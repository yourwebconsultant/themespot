# Security policy

## Supported versions

Only the latest version gets security fixes. Your version is `version` in the plugin's `.claude-plugin/plugin.json`, and the plugin's `CHANGELOG.md` lists every release. Update before you report, in case the problem is already fixed.

## Reporting a vulnerability

Report a vulnerability privately with GitHub's private vulnerability reporting on this repository: https://github.com/yourwebconsultant/themespot/security/advisories/new

Do not report a vulnerability in a public issue. Do not put a sign-in token, a real site's data or anyone's personal data in the report.

## What to include

- The plugin version, and your Claude Code version (`claude --version`).
- What an attacker could do, and the steps that show it: the agent, skill or tool involved, its input, and what happened.
- Whether you know of the problem being exploited or published anywhere.

## What happens next

- You get an acknowledgement within 7 days. Handling is best effort.
- Then an assessment: a fix, or the reason no fix is planned.
- There is no bug bounty.

## Coordinated disclosure

A fix is released before any advisory is published. Keep the details private until then. The advisory credits you if you want it to.

## Scope

In scope: this plugin's files (its manifest, its MCP server entry, its agents and its skills) and the ThemeSpot service they connect to, at `api.themespot.app` and `my.themespot.app`.

Out of scope, each with its own channel:

- HubSpot's platform: report to HubSpot.
- Claude Code, Claude.ai and the Claude models: report to Anthropic.
- ChatGPT: report to OpenAI.

## Support

For help and other questions: https://themespot.app/docs/support
