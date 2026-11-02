# Enemy

**Owner:** Kevin Cai. Only the owner creates or edits assets in this folder. Need a change? Ask in Discord.

## What's here

| Asset | What it does |
|---|---|
| BP_Zombie | A zombie that chases the player and dies when its HP reaches 0 |

Coming in W2: exp gems and the zombie spawner.

## How others use it

- **Zombies receive damage** through the damage interface in `Core` (see Core README).
- **Zombies damage the player:** _TBD (W2)_

## Tunable values

| Value | Where | Default |
|---|---|---|
| Move speed | BP_Zombie | _TBD_ |
| Max HP | BP_Zombie | 3 (for testing) |

## W1 tasks (due 11/8)

- [ ] **Zombies chase the player:** place 5 zombies by hand. All of them walk toward the player. Move speed is adjustable.
- [ ] **Zombie HP and death:** a zombie with 3 HP dies and disappears after exactly 3 hits of 1 damage.

## Testing tip

Edward's bullets may not be ready this week. Add a debug key that deals 1 damage to the zombies so you can test without waiting.
