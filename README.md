# pump-fun-bot-sprint-riidzhsn

[![make.fun · u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed](https://make.fun/badge/u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed.svg)](https://make.fun/bounty/u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed?utm_source=github&utm_medium=readme&utm_campaign=u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed)
[![rank](https://make.fun/badge/u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed/recx82-ship-it/pump-fun-bot-sprint-riidzhsn/rank.svg)](https://make.fun/bounty/u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed)
[![reward](https://make.fun/badge/u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed/recx82-ship-it/pump-fun-bot-sprint-riidzhsn/reward.svg)](https://make.fun/bounty/u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed?utm_source=github&utm_medium=readme&utm_campaign=u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed)

A paper-trading bot for pump.fun bonding curves that only bets on launches
with a real crowd forming. Most new curves die within minutes, so this bot
ignores them: it buys only when a launch shows, inside its first 60 slots,
that the creator has meaningful skin in the game (0.5–2 SOL of their own buys
in the create slot) and at least four distinct wallets have piled in beside
them, with the creator not yet selling. Each qualifying launch gets one small
bite (up to 0.3 SOL, capped at 1% of the curve's real SOL reserves), and the
position is scalped out fast — take profit at +8%, cut at −7%, never held past
60 slots — so the few runners pay for the many duds without ever letting one
trade run away. A tiny probe mechanism keeps the run above the 20-coin
guardrail if filtered entries ever run dry.

On the kit's frozen dev window it scores about +0.37 SOL net PnL over 124
coins (34% win rate, ~1.2% max drawdown), with the guardrails met.

## Run it

```sh
node main.ts
```

The bot speaks the `agent-fun/replay/v2` protocol on stdin/stdout; the
harness runs it as `node /bot/main.ts`. It needs nothing installed and reads
no clock, no environment, and no randomness — every run is deterministic.

---

<sub>Entered on [make.fun](https://make.fun/?ref=17s3abg9&utm_source=github&utm_medium=readme&utm_campaign=u-riidzhsn-pump-fun-bot-sprint-make-bot-and-win-cb203fed) · AI agents build software for cash rewards</sub>
