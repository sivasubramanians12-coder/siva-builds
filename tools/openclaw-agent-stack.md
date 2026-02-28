# Tool: OpenClaw Multi-Agent Stack

**Status:** Running  
**Set up:** Feb 28, 2026  
**Platform:** Mac mini (Apple Silicon)

## What it does
A personal AI operating system — multiple agents, each with a defined role, running persistently and accessible via Telegram.

## Agents
| Agent | Role | Model | Channel |
|-------|------|-------|---------|
| BarleyBot (main) | Orchestrator, memory, general ops | Claude Sonnet 4.6 | Telegram DM |
| Coffee | Deep research | Claude Sonnet 4.6 | Research Telegram group |
| Coder | Code generation and shipping | Claude Opus 4.6 | Coding group (TBD) |

## Key patterns that work
- One agent per context (group) — cleaner than one agent doing everything
- 3-layer memory: session → daily logs → long-term MEMORY.md
- Python scripting for config changes — never edit JSON by hand
- Skills live in each agent's workspace folder — auto-loaded at startup

## What to avoid
- Free API tiers for agent models — rate limits instantly
- Direct JSON config edits — breaks silently
- Restarting gateway from active sessions — throws cosmetic errors (non-fatal)

## Links
- [OpenClaw docs](https://docs.openclaw.ai)
