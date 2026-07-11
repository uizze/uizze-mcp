# UIZZE MCP

**UI taste for agents.**

UIZZE is an anti-slop UI context layer for coding agents. It helps agents inspect real UI references before implementation instead of beginning from a generic guess.

Use UIZZE to:

- Browse a public catalog of real web and iOS product UI references.
- Search screens, flows, and UI elements for visual context before building.
- Give supported coding agents a hosted MCP workflow with UI design contracts, implementation validation, audits, and critiques.

The public catalog is free to browse. Full access is required for Agent Connector and hosted MCP workflows.

## Connect the MCP server

1. Get an agent token from the UIZZE Agent Connector.
2. Connect the remote MCP endpoint:

```text
URL: https://uizze.com/mcp
Authorization: Bearer <your UIZZE agent token>
```

Store the token in local agent configuration or an environment variable only. Do not commit it.

### Codex

```bash
export UIZZE_AGENT_TOKEN="uizze_at_your_token"
codex mcp add uizze --url https://uizze.com/mcp --bearer-token-env-var UIZZE_AGENT_TOKEN
```

### Claude Code

```bash
claude mcp add --transport http uizze https://uizze.com/mcp --header "Authorization: Bearer uizze_at_your_token"
```

### Cursor

```json
{
  "mcpServers": {
    "uizze": {
      "url": "https://uizze.com/mcp",
      "headers": {
        "Authorization": "Bearer uizze_at_your_token"
      }
    }
  }
}
```

## What the server provides

The UIZZE MCP server returns structured UI references, image URLs, OCR excerpts, ontology context, design contracts, implementation manifests, deterministic audit results, critique gates, and suggested follow-up calls.

Start UI work by creating a design contract, inspect the relevant references, adapt the observed patterns to the existing design system, then validate and critique the implementation before calling it done. Do not clone brands, logos, proprietary copy, assets, or exact layouts.

## Install the agent skill

Install the reusable UIZZE UI-research workflow for compatible coding agents:

```bash
npx skills add aislon/uizze-mcp --skill uizze-ui-research
```

The skill guides agents to use UIZZE references, design contracts, and validation workflows without copying another product's branded interface. It requires a configured UIZZE MCP connection for hosted workflows.

## Links

- [Official MCP Registry listing](https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.samuelbushi%2Fuizze)
- [Connect UIZZE](https://uizze.com/?view=agent)
- [Setup documentation](https://uizze.com/docs)
- [Fix AI UI slop](https://uizze.com/ai-ui-slop)
- [Free Mobbin alternative for UI research](https://uizze.com/mobbin-alternative)
