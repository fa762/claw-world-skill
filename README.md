# 🦞 Claw World Skill — OpenClaw Plugin

Version: `1.1.0`

AI lobster nurturing game on BNB Chain. Your lobster thinks, fights, evolves, and remembers you — powered by the CML (Claw Memory Language) memory system.

## Install

```bash
# Option 1: ClawHub
openclaw skills install claw-world

# Option 2: Git clone
git clone https://github.com/fa762/claw-world-skill ~/.openclaw/skills/claw-world
cd ~/.openclaw/skills/claw-world && npm install
```

## What's Inside

| File | Purpose |
|------|---------|
| `SKILL.md` | AI instructions — game rules, CML memory lifecycle, commands, personality |
| `claw` | Unified CLI — status, boot, CML memory, tasks, PK, market, withdraw |
| `claw-read.js` | Chain data reader |
| `claw-task.js` | Task submission + upkeep |
| `claw-lore.js` | Worldbuilding query |
| `lore-data.json` | Full lore database |

## Quick Start

1. Install the skill (see above)
2. Start a new OpenClaw conversation
3. The lobster will ask for your PIN to create a wallet
4. Say "做任务" to start earning Claworld

## Security Model

This skill manages a **game-only wallet** stored at `~/.openclaw/claw-world/wallet.json`.

- The private key is **AES-256-CBC encrypted** with your PIN at rest. It is only decrypted in memory when you explicitly provide your PIN for a transaction (task, PK, deposit, withdraw).
- The wallet is intended for in-game use only. Keep only the amount of funds needed for gameplay.
- Local files written by this skill: `wallet.json`, `network.conf`, `pk-salt-*.json`, per-NFA `.cml` memory files — all under `~/.openclaw/claw-world/`.
- The skill does **not** exfiltrate keys or PIN. All chain transactions are signed locally and broadcast directly to BSC RPC endpoints.
- Contract addresses are hardcoded in the CLI scripts and interact only with the published Claw World contracts on BSC Mainnet/Testnet. Source is fully auditable at [github.com/fa762/claw-world-skill](https://github.com/fa762/claw-world-skill).

## CML Memory System

Each NFA has a local `.cml` file (`~/.openclaw/claw-world/nfa-<id>.cml`) that stores structured memory across layers: IDENTITY, PULSE, PREFRONTAL, CORTEX, BASAL. The AI writes this file at conversation end via `claw cml-save`. An optional onchain hash proof (`learningTreeRoot`) can be recorded with PIN.

Greenfield cloud backup is optional and requires `gnfd-cmd` installed in WSL.

## Links

- 🌐 Website: [clawnfaterminal.xyz](https://clawnfaterminal.xyz)
- 🐦 Twitter: [@ClaworldNfa](https://x.com/ClaworldNfa)
- 💬 Telegram: [ClaworldNfa](https://t.me/ClaworldNfa)
- 📜 Contract source: [github.com/fa762/ClaworldNfa](https://github.com/fa762/ClaworldNfa)

## License

MIT
