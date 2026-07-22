# UIZZE MCP

[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/uizze/uizze-mcp/badge)](https://scorecard.dev/viewer/?uri=github.com/uizze/uizze-mcp)
[![UIZZE on Smithery](https://smithery.ai/badge/smlbushi/uizze)](https://smithery.ai/servers/smlbushi/uizze)

## STOP UI SLOP.

**If your UI looks AI-generated, you've already lost the first impression.**

UIZZE arms Codex, Claude Code, Cursor, and Copilot with 800,000+ real web and iOS interfaces, live reference search, product-specific design contracts, validation, audits, and a hard finish gate before generic UI reaches users.

**[STOP UI SLOP →](https://uizze.com)**

<table>
  <tr>
    <th>Without product evidence</th>
    <th>Grounded with UIZZE</th>
  </tr>
  <tr>
    <td><img src="https://uizze.com/landing/before-uizze-simple-no-island.png" alt="Generic mobile interface created without UIZZE evidence" width="360"></td>
    <td><img src="https://uizze.com/landing/after-uizze-simple-no-island.png" alt="Product-specific mobile interface grounded with UIZZE evidence" width="360"></td>
  </tr>
</table>

## Install the free UIZZE anti-slop skill

Give Codex, Claude Code, or Cursor a workflow grounded in 800,000+ real web and iOS screens, a design contract, and a hard finish gate:

```bash
npx skills add https://uizze.com --skill anti-ui-slop
```

The free skill works on its own. Connect the hosted UIZZE MCP when you want live search, reference packs, audits, and screenshot critique inside the agent. The repository also includes the focused `uizze-ui-research` and `ui-slop-review` skills.

→ [Read the anti-slop UI workflow](ANTI_SLOP_UI_WORKFLOW.md)

→ [Run the AI UI slop preflight checklist](AI_UI_SLOP_CHECKLIST.md)

→ [Copy an anti-slop UI research, contract, validation, and critique prompt](AI_UI_SLOP_PROMPT_PACK.md)

→ [Follow the UI reference cookbook for coding agents](UI_REFERENCE_COOKBOOK.md)

Use UIZZE to:

- Browse a public catalog of real web and iOS product UI references.
- Search screens, flows, and UI elements for visual context before building.
- Give supported coding agents a hosted MCP workflow with UI design contracts, implementation validation, audits, and critiques.

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

## Links

- [Official MCP Registry listing](https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.samuelbushi%2Fuizze)
- [Connect UIZZE](https://uizze.com)
- [Setup documentation](https://uizze.com/docs)
- [STOP UI SLOP](https://uizze.com/ai-ui-slop)
- [UI research for coding agents](https://uizze.com/mobbin-alternative)
- [UIZZE vs. Refero for coding-agent workflows](https://uizze.com/refero-alternative)
- [UIZZE vs. Gummble for coding-agent workflows](https://uizze.com/gummble-alternative)
