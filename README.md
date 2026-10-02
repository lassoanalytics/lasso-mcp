# Lasso MCP

Remote MCP server for affiliate-link opportunities, link health, clicks, and content audits.

The server is hosted. This repository is the public install pointer. There is no local package and no npm install.

| | |
|---|---|
| Endpoint | `https://lasso.link/mcp` |
| Transport | Streamable HTTP |
| Docs | https://getlasso.co/mcp |
| Machine config | https://getlasso.co/mcp/config.json |
| llms.txt | https://getlasso.co/llms.txt |
| Official registry | `co.getlasso/mcp` |
| Auth | `Authorization: Bearer <LICENSE_KEY>` or OAuth (ChatGPT) |
| Get a key | https://app.getlasso.co/websites |
| Account | Free. No card. One key, one site. |
| Writes | Dry-run until you confirm in the chat. |

`initialize` answers without a key. Tool calls need the license key for the site you want to read.

## Cursor

```json
{
  "mcpServers": {
    "lasso": {
      "url": "https://lasso.link/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_LICENSE_KEY"
      }
    }
  }
}
```

## Claude Code

```bash
claude mcp add --transport http lasso https://lasso.link/mcp \
  --header "Authorization: Bearer YOUR_LICENSE_KEY"
```

## First prompt

Connect Lasso MCP. List alerts and opportunities. Dry-run the top 10 Lasso Opportunities or unmonetized links. Do not change anything until I confirm.
