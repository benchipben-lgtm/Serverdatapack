# Datapack Progress Report

Last updated: 2026-11-09

This file tracks what has been added, what is being worked on, and what still needs testing.

## Completed

- [x] Initial datapack structure and README.
- [x] Custom ore-generation changes added to the datapack.
- [x] Trident crafting recipe using a Tide Armor Trim template.
- [x] Heavy Core crafting recipe:
  ```
   E
  INI
   D
  ```
  - E = Ender Eye
  - I = Iron Block
  - N = Netherite Block
  - D = Diamond Block
  - Output = 1 Heavy Core

## Vein miner — technical investigation

<badge>Not implemented</badge>

The requested behavior is defined:

- Ore chains must include only connected blocks of the exact same ore type.
- Adjacent, different ore types must never be included.
- Connected tree logs should chain only when the player is holding an axe.
- Chain mining needs a reasonable block cap.

**Implementation blocker:** a normal Java datapack advancement can detect that a player mined a block and run a reward function, but that function runs at the player's position. The advancement reward does not pass the mined block's coordinates into the function. Without the starting block position, a function-only datapack cannot reliably flood-fill the exact connected vein or tree. A rough scan around the player would be unreliable and could mine the wrong blocks, so it is not being added as if it were a proper vein miner.

References:
- [Minecraft Wiki — Advancement definition](https://minecraft.wiki/w/Advancement_definition)
- [Minecraft Data Packs Guide — advancement reward functions](https://maybenotconnor.github.io/minecraft-data-packs-guide/ch19.html)

**Next step:** confirm the Aternos server software. If it supports a compatible server-side extension, the exact behavior can be implemented there; otherwise, we should choose a different approach rather than ship a broken datapack workaround.

## Not yet verified

- [ ] Confirm datapack compatibility with the target Minecraft server version (26.3).
- [ ] Test every custom recipe in-game.
- [ ] Test ore generation in newly generated chunks.
- [ ] Implement and test vein mining using a suitable server-side approach.
- [ ] Confirm the datapack loads without errors on the Aternos server.

## Notes

- World-generation changes affect newly generated chunks, not chunks that already exist.
- Ore-generation adjustments are intended settings and have not been confirmed by measured in-game generation tests.
- This report will be updated as features are implemented and tested.
