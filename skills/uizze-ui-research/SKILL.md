---
name: uizze-ui-research
description: Use when building, reviewing, or improving a web or iOS product UI and you need real UI references, explicit design constraints, or implementation validation through UIZZE.
version: 1.0.0
tags: [ui-design, ui-research, mcp, agent-workflows]
---

# UIZZE UI Research

Use UIZZE to give a coding agent visual product context before implementation instead of relying on a generic styling prompt.

## Prerequisites

- The public UIZZE catalog is free to browse at https://uizze.com.
- Hosted UIZZE MCP workflows require full access and a UIZZE agent token.
- Connect the remote MCP endpoint at `https://uizze.com/mcp` with `Authorization: Bearer <UIZZE agent token>` before attempting MCP work. Setup details: https://uizze.com/docs.

## Workflow

1. Use the available UIZZE tools to find relevant real web or iOS UI references, screens, flows, or elements before writing implementation code.
2. Inspect the returned references for transferable interaction and layout patterns, then adapt them to the project's existing design system.
3. Create or use a structured design contract when the UI work needs explicit constraints or acceptance criteria.
4. Implement the UI without cloning another product's brand, logo, proprietary copy, assets, or exact layout.
5. Run the available UIZZE validation, audit, or critique workflow before calling the UI work complete; address the resulting issues in the project rather than treating the reference as a template to copy.

## Use this skill for

- Designing a new product screen, flow, or component.
- Reducing generic or repetitive AI-generated UI.
- Reviewing an implementation against an explicit design contract.
- Finding real product UI context for web or iOS work.

## Do not use this skill for

- Reproducing a competitor's branded interface.
- Bypassing UIZZE access controls or exposing an agent token.
- Treating screenshots as reusable assets or copying proprietary text.
