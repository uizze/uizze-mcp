# UIZZE MCP

**UI taste for agents.**

Codex can write the UI; UIZZE helps it stop shipping generic AI UI slop. UIZZE gives Codex real web and iOS interface references before implementation, then provides design contracts, validation, audits, and critiques. Claude Code and Cursor use the same hosted MCP workflow.

## Install the UIZZE anti-AI-UI-slop skill

Give Codex, Claude Code, or Cursor UIZZE's paid anti-slop workflow:

```bash
npx skills add https://uizze.com --skill anti-ui-slop
```

The canonical first-party skill is `anti-ui-slop` from `uizze.com`. The repository also includes the focused `uizze-ui-research` and `ui-slop-review` skills.

→ [Read the anti-slop UI workflow](ANTI_SLOP_UI_WORKFLOW.md)

→ [Run the AI UI slop preflight checklist](AI_UI_SLOP_CHECKLIST.md)

→ [Copy an anti-slop UI research, contract, validation, and critique prompt](AI_UI_SLOP_PROMPT_PACK.md)

→ [Follow the UI reference cookbook for coding agents](UI_REFERENCE_COOKBOOK.md)

Use UIZZE to:

- Browse a public catalog of real web and iOS product UI references.
- Search screens, flows, and UI elements for visual context before building.
- Give supported coding agents a hosted MCP workflow with UI design contracts, implementation validation, audits, and critiques.

UIZZE has no free plan. Paid access is required for the catalog, Agent Connector, and hosted MCP workflows.

## Partner with UIZZE

Refer product builders who need real UI references and agent-ready design context. UIZZE affiliates earn **50% of each referred buyer's first paid order**, with a 30-day hold and manual payout.

[Get your referral link](https://uizze.com/affiliates)

[Use the disclosure-safe partner share kit](PARTNER_SHARE_KIT.md)

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
- [Fix AI UI slop](https://uizze.com/ai-ui-slop)
- [UI research for coding agents](https://uizze.com/mobbin-alternative)
