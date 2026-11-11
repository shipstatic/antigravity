# ShipStatic for Antigravity

Deploy static websites, landing pages, and prototypes instantly from [Antigravity](https://antigravity.google). Free, no account needed.

Ask Antigravity to put your site online, and get back a real link you can share in seconds.

## Try it in seconds, no account needed

```bash
agy plugin install https://github.com/shipstatic/antigravity
```

Then start a new session and ask, in your own words:

- "Build this project and publish it with ShipStatic."
- "Make a one-page site for my bakery and give me a link I can share."
- "Publish the dist folder with ShipStatic's built-in password protection."

You get back a link you can share right away, and a claim link. The site stays up for 3 days, and opening the claim link keeps it for good.

Want it private? Ask for ShipStatic's built-in password protection. Visitors have to type the password before they see anything, on the site's link and on any custom domain pointing at it.

The plugin has one skill, `publish-online`, and one MCP server, `https://mcp.shipstatic.com`. Antigravity picks how the files travel:

- **A folder on disk** goes through the ShipStatic CLI, with `npx -y @shipstatic/ship@3`. It needs Node.js 20.19 or newer, and nothing to install.
- **When the CLI can't run,** a few small files go through the MCP server's `deployments_upload` tool instead.

## Keep your sites with a free account

Everything above works with no account. A free account keeps your sites for good, gives you a ShipStatic domain like `yourname.shipstatic.com`, and shows you everything you've published in one place. A custom domain like `www.example.com` needs a paid plan.

Each way Antigravity publishes has its own setup:

| | With no account (the default) | Straight into your account |
|---|---|---|
| **A folder, through the CLI** | Live for 3 days, with a claim link | Run `npx -y @shipstatic/ship@3 config` once, with an API key from [my.shipstatic.com/api-key](https://my.shipstatic.com/api-key) |
| **Files, through the MCP server** | Live for 3 days, with a claim link | Type `/plugin`, open **shipstatic** under Installed, and choose **Sign in** |

Signing in on one way doesn't set up the other. You can see and manage every site at [my.shipstatic.com](https://my.shipstatic.com).

## What the plugin runs and sends

- **It runs the ShipStatic CLI** with `npx -y @shipstatic/ship@3`, which downloads the CLI from npm.
- **It connects Antigravity to the hosted ShipStatic MCP server** at `https://mcp.shipstatic.com`, as `shipstatic_ship`.
- **It sends the files you publish to ShipStatic,** through the CLI, which uses ShipStatic's API, or through the MCP server. Nothing else is sent anywhere.
- **The claim link is yours alone.** Whoever opens it and signs in owns the site, so don't share it.

## Also available

| Surface | Reach it |
|---------|----------|
| **[MCP](https://mcp.shipstatic.com)** | Drop `https://mcp.shipstatic.com` into any MCP client |
| **[CLI and SDK](https://github.com/shipstatic/ship)** | `npx @shipstatic/ship ./dist` |
| **[VS Code](https://marketplace.visualstudio.com/items?itemName=shipstatic.shipstatic)** | Search "ShipStatic" in the Marketplace |
| **[Plugin](https://github.com/shipstatic/plugin)** | Install it in Cursor, Claude Code, Codex or Gemini CLI |
| **[OpenCode](https://github.com/shipstatic/opencode)** | `opencode plugin add opencode-shipstatic` |
| **[n8n](https://www.npmjs.com/package/n8n-nodes-shipstatic)** | Search "ShipStatic" in n8n's node panel |
| **[GitHub Action](https://github.com/shipstatic/action)** | `shipstatic/action@v3` |

[Support](https://www.shipstatic.com/support) • [Privacy](https://www.shipstatic.com/privacy) • [Terms](https://www.shipstatic.com/terms)

## License

MIT
