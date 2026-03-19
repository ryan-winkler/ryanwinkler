# Moltis, ZeroClaw, and Nemoclaw

## Summary

This is the AI tooling thread I use to pressure-test what makes an assistant useful enough to live in daily workflows.

## Current status

| Name | Status | Notes |
| --- | --- | --- |
| Moltis | Current | The live AI gateway I use now |
| ZeroClaw | Deprecated | Replaced in March 2026 |
| Nemoclaw | Emerging | A naming thread around what may come next, but not the canonical live system today |

## Why Moltis replaced ZeroClaw

ZeroClaw stopped being the right daily system for me.

The practical problems were straightforward:

- frequent crashes from invalid TOML configuration
- malformed-message spam in connected workflows
- no OpenAI-compatible API path for the Home Assistant integration work I cared about

Moltis became the better fit because it gave me a more reliable gateway, better provider flexibility, a web UI, and cleaner MCP-based integration paths.

## Why it matters now

- It is the most current public example of how I think about AI reliability, routing, and fallback paths
- The switch from ZeroClaw to Moltis is a concrete product decision, not a naming exercise
- It keeps the AI story grounded in daily utility instead of model-chasing

## Current lessons

- reliability is a product feature, not just an engineering concern
- provider failover only matters if the system remains understandable to the user
- AI stacks get better when the interface between tools is boring and explicit

## Links

- [Moltis website](https://www.moltis.org/)
- [Moltis documentation](https://docs.moltis.org/)
- [Moltis repository](https://github.com/moltis-org/moltis)

## Related project notes

- [Meitheal](meitheal.md)
- [Coolock Village Forge](coolock-village-forge.md)
