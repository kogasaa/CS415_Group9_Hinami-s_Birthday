# Hinami's Birthday — Team Rules

Everything our team makes goes inside this folder. The template folders outside it (`Characters`, `Cursor`, `LevelPrototyping`, `TopDown`) are read-only and will be deleted later.

## Folders and owners

| Folder | Owner | Contents |
|---|---|---|
| Core | Bingkun | Game rules, shared interfaces, leveling |
| Player | Edward | Player character, bullets, player stats |
| Enemy | Kevin | Zombies, exp gems, spawner |
| UI | Bo Wen | HUD, level-up screen, win/lose screen, main menu |
| Audio | Kevin | Sound effects, music |
| Art | Bingkun | Hinami character art and references |
| Maps | Bingkun (Main), everyone (own test map) | Game level and test maps |

Each folder has its own README: what's inside, how others use it, which values can be tuned, and this week's tasks.

## Folder rules

1. Only create or edit assets in your own folder.
2. Only Bingkun edits `Core` and `Maps/Main`. Need a change? Ask in Discord.
3. Test only in your own test map (`Maps/Test_YourName`). Don't place anything in `Main`.
4. Never move or rename someone else's assets. Moving assets in Unreal leaves redirectors, which cause conflicts and broken references.
5. Don't edit the template assets. Build your own versions inside this folder.

## Git rules

1. Pull before you start working.
2. Commit and push after each small piece of work. Write a clear commit message that says what you did (not just "update").
3. Before pushing, open the project in the editor and make sure it runs.
4. If something goes wrong, stop and ask in Discord. Never use `force push`.

## Naming prefixes

| Prefix | Asset type | Example |
|---|---|---|
| BP_ | Blueprint | BP_Zombie |
| WBP_ | Widget Blueprint (UI) | WBP_HUD |
| BPI_ | Blueprint Interface | BPI_Damageable |
| SPR_ | Sprite | SPR_Hinami_Idle |
| FB_ | Flipbook (2D animation) | FB_Hinami_Walk |
| T_ | Texture | T_Hinami_Sheet |
| DT_ | Data Table | DT_Abilities |
| SFX_ | Sound effect | SFX_Shoot |

## Weekly check

Every Sunday (first one: 11/8), each person demos their work to another teammate. A task only counts as done if it is pushed to the repo. "It works on my computer" doesn't count.
