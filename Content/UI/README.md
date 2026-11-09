# UI

**Owner:** Bo Wen. Only the owner creates or edits assets in this folder. Need a change? Ask in Discord.

## What's here

| Asset | What it does |
|---|---|
| WBP_HUD | On-screen info: time left and player HP |
| WBP_MainMenu | (Bonus) Main menu with a Start button |

## How others use it

- **Who adds the HUD to the screen:** `BP_HinamiGameMode` (Bingkun), per the project interface rules. On gameplay start, use `Create Widget (WBP_HUD, Owning Player = Get Player Controller 0)` followed by `Add to Viewport`. Create only one instance. This integration is still pending in Core/Main.
- `WBP_MainMenu` sets UI-only input, shows the mouse cursor, and focuses Start when constructed. Start restores game-only input, hides the cursor, and opens `/Game/Maps/Main`. Quit calls `Quit Game` (ends the play session in PIE).
- A menu entry point can create `WBP_MainMenu` and add it to the viewport. The project's default startup map has not been changed.

## Data the UI needs

| Data | Comes from | Ready in |
|---|---|---|
| Time left | Core (Bingkun) | W1 |
| Player HP | Player (Edward) | W2 |

`WBP_HUD` reads `BP_Player.GetHP()` and `GetMaxHP()` from player pawn 0 every frame, and `BP_HinamiGameMode.GetTimeLeft()` from the current GameMode. HP functions return floats; TimeLeft returns integer seconds. The bar uses HP / max(MaxHP, 1), and time displays minutes and seconds. If the casts fail, the designer defaults remain visible.

Level, EXP text, and the experience bar are visual placeholders until Core supplies those interfaces. Current stub data may remain constant; the HUD does not implement gameplay timers or damage itself.

## Tunable values

- Designer colors, font sizes, canvas anchors, and spacing in both widgets.
- MainMenu Start event: destination level `/Game/Maps/Main`.
- HUD designer fallback values: `100 / 100 HP`, `05:00`, `LEVEL 01`, `EXP 0 / 100`.

## Preview and validation

Open `Content/Maps/Test_BoWen` and press Play. Its Level Blueprint creates the HUD immediately, then overlays the main menu after 8 seconds. This is a UI demo sequence, not the production startup flow.

Validated in Unreal Engine 5.4.4 on November 8, 2026:

- Both widgets and the test Level Blueprint compile successfully and are saved.
- HUD renders in PIE; time reads `10:00` from the current GameMode, and HP displays `100 / 100 HP`.
- Main menu renders with its cake illustration and both buttons.
- Start loads `/Game/Maps/Main` (confirmed in the editor log).
- Quit ends PIE successfully.

Main currently does not spawn the HUD; the Core owner should add the creation step above. No Core or Main assets were edited for this UI demo. Health changes, countdown progression, and packaged builds have not been tested.

## W1 tasks (due 11/8)

- [x] **HUD:** time left and player HP are shown on screen, with calls to the shared data functions.
- [x] **(Bonus) Main menu:** Start opens Main; Quit ends the game.
