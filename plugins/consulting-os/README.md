# Consulting OS

Jonathan Chan's consulting method library for Claude, from [AI Never Sleeps](https://www.aineversleeps.net). It covers 51 methods, from framing a vague brief and building the issue tree to the model, the storyline and the final deck. Each method is a full playbook: when to use it, the steps, worked examples and the checks to run before anything reaches a client.

The methods are served live to Claude from AI Never Sleeps, so every member always has the current version. When the models change, the library changes, and there's nothing to reinstall.

**Requires a Consulting OS membership.** It's included with [The Consulting AI Operating System](https://www.aineversleeps.net/consulting-ai-os), or [on its own](https://www.aineversleeps.net/consulting-os). You sign in with the email you bought with. Full guide: [aineversleeps.net/consulting-os/setup](https://www.aineversleeps.net/consulting-os/setup).

## What's inside

- **The `consulting-os` skill.** It tells Claude when to reach for the library and how to use it: pick the method, follow it step by step, de-identify client material first, and check every number before it leaves your hands.
- **The `consulting-os` connector.** A remote MCP server at `https://www.aineversleeps.net/api/consulting-os/mcp` with five read-only tools: `list_methods`, `find_methods`, `get_method`, `get_method_file` and `whats_new`.

The plugin runs no local code. It has no hooks, commands, agents or scripts: just the skill file and the connector address.

## Install in Claude Code

```text
/plugin marketplace add AINeverSleeps/ains-plugins
/plugin install consulting-os@aineversleeps
/mcp
```

In `/mcp`, pick **consulting-os** and choose Authenticate. A browser window opens: sign in with your membership email, open the emailed link in the same browser, and you're connected.

## Use it in the Claude app (web, desktop, Cowork)

1. Open **Customize > Connectors** and choose **Add custom connector**.
2. Name: `Consulting OS`. URL: `https://www.aineversleeps.net/api/consulting-os/mcp`
3. Click **Add**, then **Connect**, and sign in with your membership email.

On a Team or Enterprise plan, an Owner adds the connector first (Organization settings > Connectors), then members click Connect.

## Things to try

- "Use Consulting OS to frame this problem and give me a day-one answer: a regional bank takes 21 days to approve a mortgage and its competitors take 7."
- "Use Consulting OS to build an issue tree for why our gross margin fell 4 points last year."
- "Use Consulting OS to size the Australian market for commercial EV chargers, back of the envelope."

## What it sends and receives

- **Sign-in:** OAuth 2.1 with AI Never Sleeps (aineversleeps.net). The connector receives your sign-in email so it can check your membership.
- **Requests:** the method names Claude asks for, plus a short task description when it searches for a method (for example "size a market").
- **Responses:** method text from the library.

Your files and full conversations stay in Claude. The connector never receives them. See the [privacy policy](https://www.aineversleeps.net/privacy-policy).

## Support

Email jonathan@aineversleeps.net.

## Licence

The plugin wrapper in this folder is released under the MIT licence (see LICENSE). The method library itself is served to members from AI Never Sleeps and is not covered by that licence: it is copyright AI Never Sleeps, all rights reserved.
