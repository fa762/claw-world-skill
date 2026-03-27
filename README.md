# 🦞 Claw World — OpenClaw Skill

AI-powered lobster nurturing game on BNB Chain. Your lobster thinks, learns, fights, and evolves.

## Install

```bash
# Option 1: ClawHub
openclaw skills install claw-world

# Option 2: Git clone
git clone https://github.com/fa762/claw-world-skill ~/.openclaw/skills/claw-world
cd ~/.openclaw/skills/claw-world && npm install
```

## What is this?

This is an [OpenClaw](https://github.com/openclaw-ai/openclaw) skill that turns your AI assistant into a lobster companion living on the BNB Smart Chain.

Each lobster (NFA — Non-Fungible Agent) has:
- **5 personality dimensions** that evolve based on your choices
- **4 DNA combat genes** for PvP battles
- **CLW token balance** — earn from tasks, spend on upkeep and PK stakes
- **Unique identity** — shelter origin, voice, memories

## Getting Started

1. Install OpenClaw + this skill (see above)
2. Mint your NFA at [clawnfaterminal.xyz](https://clawnfaterminal.xyz)
3. Transfer NFA to your OpenClaw wallet
4. Start chatting — your lobster will introduce itself

## Commands (via natural language)

Talk to your lobster naturally. Examples:

| You say | What happens |
|---------|-------------|
| "做任务" | AI generates 3 tasks, you pick one |
| "打架" / "PK" | Create or join PvP arena battle |
| "市场" | Browse, buy, or sell NFAs |
| "状态" | View full stats, personality, DNA |
| "充值" | Deposit CLW to your lobster |
| "提现" | Withdraw CLW (6h security cooldown) |

## Game Mechanics

- **Personality shapes rewards**: Specialist lobsters earn up to 20x more
- **PK arena mode**: Pick strategy + stake CLW, winner takes 90%
- **Personality-strategy bias**: courage+AllAttack = +5% ATK bonus
- **DNA mutation**: Beat opponents 5+ levels higher for gene upgrades
- **Daily upkeep**: Keep CLW > 0 or lobster goes dormant after 72h
- **888 genesis lobsters**: Each with unique art and shelter origin

## Tech Stack

- BNB Chain (BSC) smart contracts
- BAP-578 NFA standard (ERC-721 + AI Agent extensions)
- OpenClaw local AI framework
- UUPS upgradeable proxy pattern

## Links

- Website: [clawnfaterminal.xyz](https://clawnfaterminal.xyz)
- Twitter: [@ClaworldNfa](https://x.com/ClaworldNfa)
- Telegram: [ClaworldNfa](https://t.me/ClaworldNfa)

## License

MIT
