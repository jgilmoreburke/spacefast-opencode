# Spacefast for OpenCode

Publish to the web from OpenCode. Spacefast gives your agent a remote MCP server that builds, hosts, and shares sites and apps — with a real database, custom domains, and instant live URLs.

Ask OpenCode to "build a landing page and publish it with Spacefast" and you get back a live `*.space.fast` URL.

**Demo:** [oc-test.space.fast](https://oc-test.space.fast/) — built and published from OpenCode using its free default model.

## What you can do

- Create a site or app from a prompt and publish it to a live URL
- Update an existing space and republish
- Share spaces, manage versions, and connect custom domains
- Use a built-in database for apps (not just static pages)

## Install

### 1. Add the Spacefast MCP server

Add this to your global OpenCode config at `~/.config/opencode/opencode.json`, or to `opencode.json` in a project:

```json
{
  "$schema": "https://opencode.ai/config.json",
  "mcp": {
    "spacefast": {
      "type": "remote",
      "url": "https://mcp.spacefast.com",
      "enabled": true
    }
  }
}
```

If you already have an `opencode.json`, merge the `spacefast` entry into your existing `mcp` block instead of overwriting the file.

### 2. Sign in

```bash
opencode mcp auth spacefast
```

This opens your browser to sign in to Spacefast (OAuth).

### 3. Check it's connected

```bash
opencode mcp list
```

Start `opencode` — the footer should show `1 MCP`.

## Try it

```
Create a one-page site about local hiking trails and publish it with Spacefast.
```

OpenCode will ask before each Spacefast tool call. Approve them, and it returns a live URL.

## Links

- Spacefast: https://spacefast.com
- OpenCode MCP docs: https://opencode.ai/docs/mcp-servers/

## License

MIT — see [LICENSE](LICENSE).
