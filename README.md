# CS415\_Group9\_Hinami's\_Birthday

# 

# Team Rules

Everything our team makes goes inside this folder. The template folders outside it (`Characters`, `Cursor`, `LevelPrototyping`, `TopDown`) are read-only and will be deleted later.

## Folders and owners

|Folder|Owner|Contents|
|-|-|-|
|Core|Bingkun|Game rules, shared interfaces, leveling|
|Player|Edward|Player character, bullets, player stats|
|Enemy|Kevin|Zombies, exp gems, spawner|
|UI|Bo Wen|HUD, level-up screen, win/lose screen, main menu|
|Audio|Kevin|Sound effects, music|
|Art|Bingkun|Hinami character art and references|
|Maps|Bingkun (Main), everyone (own test map)|Game level and test maps|

Each folder has its own README: what's inside, how others use it, which values can be tuned, and this week's tasks.

## Folder rules

1. Only create or edit assets in your own folder.
2. Only Bingkun edits `Core` and `Maps/Main`. Need a change? Ask in Discord.
3. Test only in your own test map (`Maps/Test\\\\\\\_YourName`). Don't place anything in `Main`.
4. Never move or rename someone else's assets. Moving assets in Unreal leaves redirectors, which cause conflicts and broken references.
5. Don't edit the template assets. Build your own versions inside this folder.

## Git rules

1. Pull before you start working.
2. Commit and push after each small piece of work. Write a clear commit message that says what you did (not just "update").
3. Before pushing, open the project in the editor and make sure it runs.
4. If something goes wrong, stop and ask in Discord. Never use `force push`.

## Naming prefixes

|Prefix|Asset type|Example|
|-|-|-|
|BP\_|Blueprint|BP\_Zombie|
|WBP\_|Widget Blueprint (UI)|WBP\_HUD|
|BPI\_|Blueprint Interface|BPI\_Damageable|
|SPR\_|Sprite|SPR\_Hinami\_Idle|
|FB\_|Flipbook (2D animation)|FB\_Hinami\_Walk|
|T\_|Texture|T\_Hinami\_Sheet|
|DT\_|Data Table|DT\_Abilities|
|SFX\_|Sound effect|SFX\_Shoot|

## Weekly check

Every Sunday (first one: 11/8), each person demos their work to another teammate. A task only counts as done if it is pushed to the repo. "It works on my computer" doesn't count.



## Interface Rules

1. Game plane: XY (flat ground). The camera looks straight down and uses orthographic projection. Sprites are rotated to lie flat.
2. Damage: Use Unreal's built-in damage system. The attacker calls Apply Damage; the target handles Event AnyDamage (HP loss, invincibility, death).
3. Tags: Zombies have the tag Enemy; the player has the tag Player. Bullets only damage Enemy; zombies only damage Player.
4. Exp: To talk to Core, always go through the GameMode. When an exp gem touches the Player, it calls AddExp(Amount) on BP\_HinamiGameMode, then destroys itself.
5. HUD: Data lives with its owner, and the HUD reads it every frame. Time left comes from GetTimeLeft() on BP\_HinamiGameMode; HP comes from GetHP() and GetMaxHP() on BP\_Player. BP\_HinamiGameMode creates WBP\_HUD when the game starts.
6. Stubs: Shared functions (AddExp, GetTimeLeft, GetHP, GetMaxHP) are created as empty stubs in W1, so others can call them right away.

