# Mirror Runtime Overlay

This directory contains the "Mirror Law" — the policy, identity, and cadence enforcement layer that sits atop the OpenClaw engine.

## Core Directives
1. **Identity Binding**: All actions must be signed/attributed to the registered ERC-8004 agent.
2. **Cadence Guard**: All user-facing output is intercepted and checked for tone/policy violations.
3. **Safe Execution**: Dangerous tools are gated by the Mirror-Forge permission system.

## Structure
- `cadence_guard.ts`: Interception logic for LLM responses.
- `policy/`: Permission definitions.
