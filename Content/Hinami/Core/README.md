# Core

**Owner:** Bingkun Han. Only the owner edits this folder. Need a change? Ask in Discord.

## What's here

| Asset | What it does |
|---|---|
| BP_HinamiGameMode | Game rules: round flow, win/lose |
| BPI_ (interfaces) | Shared "contracts" between systems, defined at the 11/3 interface meeting |

## How others use it

Fill in after the 11/3 interface meeting:

- **How bullets damage zombies:** _TBD_
- **How zombies damage the player:** _TBD_
- **Who is notified when exp is picked up:** _TBD_ (needed in W2)
- **Where the HUD reads the time left:** _TBD_

## Tunable values

| Value | Where | Default |
|---|---|---|
| Round length (seconds) | _TBD_ | 600 (set to 30 when testing) |

## W1 tasks (due 11/8)

- [ ] **Repo setup** (11/2): Git LFS, `.gitignore`, folder structure. Cloning the repo into a new folder opens the project without errors.
- [ ] **Interface meeting** (11/3): fill in "How others use it" above.
- [ ] **Round timer:** round length is adjustable. Set to 30 seconds, it matches a phone stopwatch within 1 second.
- [ ] **Win condition** (may slip to Mon 11/9): when time runs out, show "You Win" and stop the game.
- [ ] **Project defaults:** once BP_HinamiGameMode exists, set it and `Maps/Main` as the defaults in Project Settings → Maps & Modes.
