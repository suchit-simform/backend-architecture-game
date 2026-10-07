# Backend Architecture Game

Pick the building blocks of a backend in four short rounds: API, Database, Auth, Caching. You leave with a decision record (ADR) and a scaffold.

## Install

1. Copy `backend-architect-game.md` into `.claude/commands/`.
2. Keep this file elsewhere (for example `docs/`). Any `.md` in that folder becomes a command.
3. Run `/backend-architect-game`.

## How it works

1. Answer two questions: what you're building, and your stack.
2. Play four rounds: API, Database, Auth, Caching.
3. Each round: scenario, your pick, a twist, a tradeoff table.
4. A boss round checks that your picks fit together.
5. You get `ADR.md` and a scaffold.

## Walkthrough

One round, in short:

> **Game:** Two developers, and a mobile app is coming. Pick one: 1. REST 2. GraphQL 3. tRPC

> **You:** 1

> **Game:** Twist: mobile screens now need data from five resources. Still REST?

> **You:** Yes, I'd add a few aggregate endpoints.

> **Game:** _(tradeoff table)_ 🎯 Right-sized. +10 XP.

Stuck at any point? Type `hint`.

## Video Walkthrough

- [Demo Video Link](https://drive.google.com/file/d/15nUnyOS1rp-lDKfJVTrvpWHJA6A9__qy/view?usp=sharing)

## Commands

| In game             | What it does                        |
| ------------------- | ----------------------------------- |
| `hint`              | A nudge. Repeat for a stronger one. |
| `explain <option>`  | Short deep-dive on one option       |
| `compare <a> <b>`   | Side-by-side of two options         |
| `harder` / `easier` | Change difficulty                   |
| `status`            | Show your progress                  |
| `pause`             | Save and stop                       |
| `help`              | List these commands                 |

| Option           | What it does                                                                                |
| ---------------- | ------------------------------------------------------------------------------------------- |
| `--help`         | Show help and stop                                                                          |
| `--phase <name>` | Start at a phase: `setup`, `calibration`, `api`, `db`, `auth`, `caching`, `boss`, `outputs` |
| `--stack <name>` | Skip the stack question (new games)                                                         |
| `--continue`     | Resume your save                                                                            |
| `--reset`        | Erase your save and start over                                                              |

## Badges and XP

Badges: 🎯 Right-sized, 🏗️ Over-engineered, ⚠️ Under-engineered, 🔮 Future-proofed.

XP is just a progress counter: +10 per completed round, 40 in total.

## Saving

Progress saves automatically to `.backend-architect-game/progress.json`. Run the command again to resume.

## Troubleshooting

- **Started over instead of resuming:** check that the save folder above exists. Older versions used `.architect-game/`; rename it.
- **Want a different stack:** run with `--reset`.
- **Want to redo one layer:** run with `--phase <layer>`.
