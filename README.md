# AI Never Sleeps: Claude plugins

Claude plugins from [AI Never Sleeps](https://www.aineversleeps.net) (Jonathan Chan).

## Consulting OS

The consulting method library from The Consulting AI Operating System. It covers 51 methods, from framing a vague brief and building the issue tree to the model, the storyline and the final deck. The methods are served live to Claude from AI Never Sleeps, so every member always has the current version. When the models change, the library changes, and there's nothing to reinstall.

**Requires a Consulting OS membership.** It's included with [The Consulting AI Operating System](https://www.aineversleeps.net/consulting-ai-os), or [on its own](https://www.aineversleeps.net/consulting-os). You sign in with the email you bought with. Full guide: [aineversleeps.net/consulting-os/setup](https://www.aineversleeps.net/consulting-os/setup).

### Use it in the Claude app (web, desktop, Cowork)

1. Open **Customize > Connectors** and choose **Add custom connector**.
2. Name: `Consulting OS`. URL: `https://www.aineversleeps.net/api/consulting-os/mcp`
3. Click **Add**, then **Connect**.
4. Sign in with the email you bought with. Open the emailed link in the same browser and you'll go straight back to Claude, connected.

Then start a new chat and ask, for example: *"Use Consulting OS to frame this problem and give me a day-one answer: ..."*

On a Team or Enterprise plan, an Owner adds the connector first (Organization settings > Connectors), then members click Connect.

### Install in Claude Code

```text
/plugin marketplace add AINeverSleeps/ains-plugins
/plugin install consulting-os@aineversleeps
/mcp
```

In `/mcp`, pick **consulting-os** and choose Authenticate.

To get plugin updates automatically, open `/plugin`, go to Marketplaces, select **aineversleeps** and choose **Enable auto-update**. The methods themselves always come live from the server, so you get those updates either way.

Tools that can't sign in (VS Code Copilot, your own scripts) can use an API key from [aineversleeps.net/members/consulting-os](https://www.aineversleeps.net/members/consulting-os), sent as `Authorization: Bearer <key>`.

### What's inside

- **The `consulting-os` skill.** It tells Claude when to reach for the library and how to use it: pick the method, follow it step by step, de-identify client material first, and check every number before it leaves your hands.
- **The `consulting-os` connector.** It's a remote MCP server with five read-only tools: `list_methods`, `find_methods`, `get_method`, `get_method_file` and `whats_new`.

### Your data

The connector receives the method names and search words Claude sends it, plus your sign-in email so it can check your membership. Your documents and conversations stay in Claude. See the [privacy policy](https://www.aineversleeps.net/privacy-policy).

### Support

Email jonathan@aineversleeps.net.

---

This repository holds the plugin wrapper only, released under the MIT licence (see LICENSE). The method library itself is served to members from AI Never Sleeps and is not covered by that licence: it is copyright AI Never Sleeps, all rights reserved.
