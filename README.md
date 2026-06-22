# PokerBot — SneakPeek Hold'em Agent

An autonomous poker-playing agent built for the **IIT Pokerbots Competition**, where bots face off in heads-up matches of **SneakPeek Hold'em**, a variant of Texas Hold'em.

Decision-making blends opponent modeling, probability-based hand evaluation, and rule-driven betting logic to choose actions at each stage of a hand. The full breakdown of how the bot reasons through a hand — from preflop ranges to postflop danger assessment — lives in [`docs/`](docs).

## Layout

```
PokerBot/
├── bots/
│   └── submission.py        # competition bot entry point
├── engine/                  # match engine supplied by the competition
│   ├── engine.py
│   ├── example_bot.py
│   ├── config.py
│   └── pkbot/               # engine internals (states, actions, runner)
├── evaluation/
│   └── tournament.py        # runs automated matches between bots
├── docs/                    # design notes, one file per subsystem
├── requirements.txt
└── IIT_Pokerbots_Certificate.png
```

## Getting started

```bash
pip install -r requirements.txt
```

Run a head-to-head match through the engine:

```bash
cd engine
python engine.py
```

Run a batch tournament across multiple bots:

```bash
python evaluation/tournament.py
```

## Documentation

The `docs/` directory walks through the bot's internals topic by topic — constants and config, opponent modeling, equity/hand-strength estimation, board-texture and danger detection, preflop and postflop strategy, helper utilities, and a final strategic summary tying it all together.

## Background

Built as a submission to the IIT Pokerbots Competition (certificate included above).
