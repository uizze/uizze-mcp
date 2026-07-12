# UI reference cookbook for coding agents

AI can produce a functional interface quickly. The hard part is giving it enough product context to avoid a generic first draft. UIZZE gives supported coding agents a way to research real web and iOS interface references before implementation, then work from a design contract and validate the result.

The public UIZZE catalog is free to browse. A UIZZE agent token and full access are required for Agent Connector and hosted MCP workflows.

## Use it before the first UI commit

Connect UIZZE to Codex, Claude Code, or Cursor, then give the agent a feature-specific research brief. Start narrow: the UI job, platform, user intent, product constraints, and the decision that needs evidence.

```text
I am adding [feature] to an existing [web/iOS] product.

Before proposing UI, use UIZZE to research real references for [specific UI job]
and separate observed evidence from assumptions. Then create a design contract that
fits our existing design system. Do not reproduce another product's brand, copy,
assets, or exact layout.
```

Example UI jobs:

- A billing upgrade moment that explains the value before the plan selector.
- A mobile empty state that gets a new user to a meaningful first action.
- A settings flow that makes irreversible choices understandable.
- A search result that shows confidence, scope, and a useful next step.

## Turn research into a buildable contract

References are input, not a specification to copy. Once the relevant patterns are identified, ask the agent to turn the useful observations into decisions your product can own.

```text
Use the UIZZE research to create a compact design contract for this feature.
Include the user goal, hierarchy, information needed before action, required states,
interaction risks, responsive behavior, and what must remain consistent with our
design system. Flag anything that is an assumption.
```

A good contract makes it clear what an implementation must accomplish even when its visual language, wording, components, and content are unique to your product.

## Audit the rendered interface before shipping

After implementation, use the contract as the quality bar. The goal is not pixel matching; it is evidence-backed critique of whether the UI solves the intended problem with enough clarity and product-specific intent.

```text
Review this rendered implementation against its design contract.
Identify blocking gaps, missing states, generic decisions, observable responsive or
accessibility issues, and design-system inconsistencies. Separate verified findings
from unverified concerns and give the smallest useful next action for each finding.
```

## The anti-slop loop

```text
UI job → real references → product-specific contract → implementation → audit → focused critique
```

This loop keeps agents grounded in real interface evidence while preserving your product's own brand and design system.

## Connect UIZZE

```text
URL: https://uizze.com/mcp
Authorization: Bearer <your UIZZE agent token>
```

For the complete configuration examples, see the [README](README.md). For copy-ready research, contract, validation, and critique prompts, see the [AI UI slop prompt pack](AI_UI_SLOP_PROMPT_PACK.md). The standalone [AI UI slop review skill](skills/ai-ui-slop-review/SKILL.md) is free to install and use without a UIZZE connection.

## Explore UIZZE

- [Browse the free UI reference catalog](https://uizze.com/mobbin-alternative?utm_source=github&utm_medium=referral&utm_campaign=ui_reference_cookbook)
- [Learn about the anti-slop UI workflow](https://uizze.com/ai-ui-slop?utm_source=github&utm_medium=referral&utm_campaign=ui_reference_cookbook)
- [Connect the Agent Connector](https://uizze.com/?view=agent&utm_source=github&utm_medium=referral&utm_campaign=ui_reference_cookbook)
