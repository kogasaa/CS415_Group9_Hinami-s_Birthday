# Player

**Owner:** Edward Shang. Only the owner creates or edits assets in this folder. Need a change? Ask in Discord.

## What's here

| Asset | What it does |
|---|---|
| BP_Player | The 2D player character (Hinami): movement and camera |
| BP_Bullet | A bullet fired toward the mouse cursor |

## How others use it

- **Bullets → zombies:** bullets deal damage through the damage interface in `Core` (see Core README).
- **Zombies → player:** _TBD at the 11/3 interface meeting_
- **Player HP for the HUD (Bo Wen):** _TBD (W2)_

## Tunable values

| Value | Where | Default |
|---|---|---|
| Move speed | BP_Player | _TBD_ |
| Fire rate | _TBD_ | _TBD_ |
| Bullet speed | BP_Bullet | _TBD_ |
| Bullet lifetime | BP_Bullet | _TBD_ |

## W1 tasks (due 11/8)

- [ ] **8-direction movement + camera follow:** moving diagonally is not faster than moving straight. Move speed is a variable, and changes take effect right away.
- [ ] **Mouse aim + shooting** (may slip to Tue 11/10): hold the left mouse button to fire toward the cursor. Fire rate is adjustable. After firing for 1 minute, the number of bullets in the level does not keep growing.

## Notes

- Don't edit the template character in `TopDown/`. It is 3D and uses click-to-move. Build your own 2D character here.
