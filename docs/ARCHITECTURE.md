# Mirror Runtime Architecture

## Philosophy
**Engine = OpenClaw** (Upstream)
**Law = Mirror** (Overlay)

We minimize changes to the `src/` directory to ensure we can easily merge upstream updates. All custom logic lives in `mirror/`.

## Response Interception
The engine's message emission loop is hooked to pass content through `mirror/cadence_guard.ts` before delivery.

## Tooling
Tools are provided by **Mirror-Forge**, a separate local daemon. The runtime accesses them via standard `exec` calls or a custom plugin.

## Identity
The runtime binds to the `AGENTS.md` onchain identity. It does not act without an identity context.
