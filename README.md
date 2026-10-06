# AI Never Sleeps: Claude plugins

Claude plugins from [AI Never Sleeps](https://www.aineversleeps.net) (Jonathan Chan).

## AINS Consulting OS

The consulting method library from The Consulting AI Operating System. It covers 51 methods, from framing a vague brief and building the issue tree to the model, the storyline and the final deck. The methods are served live to Claude from AI Never Sleeps, so every member always has the current version. When the models change, the library changes, and there's nothing to reinstall.

**Requires an AINS API key.** The key is included with [The Consulting AI Operating System](https://www.aineversleeps.net/consulting-ai-os). Members copy it from [aineversleeps.net/members/consulting-os](https://www.aineversleeps.net/members/consulting-os).

### Install in Claude Code

```text
/plugin marketplace add AINeverSleeps/ains-plugins
/plugin install consulting-os@aineversleeps
```

Paste your API key when asked. To change it later, run `/plugin configure consulting-os@aineversleeps`.

To get plugin updates automatically, open `/plugin`, go to Marketplaces, select **aineversleeps** and choose **Enable auto-update**. The methods themselves always come live from the server, so you get those updates either way.

### Use it in the Claude app (web, desktop, Cowork)

1. Open **Customize > Connectors** and choose **Add custom connector**.
2. Name: `AINS Consulting OS`
3. URL: `https://www.aineversleeps.net/api/consulting-os/mcp`
4. Authentication: **API key / bearer token**. Paste your key.

Then ask, for example: *"Use the Consulting OS to frame this problem and give me a day-one answer: ..."*

### What's inside

- **The `consulting-os` skill.** It tells Claude when to reach for the library and how to use it: pick the method, follow it step by step, de-identify client material first, and check every number before it leaves your hands.
- **The `consulting-os` connector.** It's a remote MCP server with five read-only tools: `list_methods`, `find_methods`, `get_method`, `get_method_file` and `whats_new`.

### Your data

The connector only sends method names and search words to AI Never Sleeps, to fetch methods. Your documents and conversations stay in Claude. See the [privacy policy](https://www.aineversleeps.net/privacy-policy).

### Support

Email jonathan@aineversleeps.net.

---

This repository holds the plugin wrapper only. The method library is served to members and is copyright AI Never Sleeps. All rights reserved.
