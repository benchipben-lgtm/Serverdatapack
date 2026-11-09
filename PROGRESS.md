# Datapack Progress Report

Last updated: 2026-11-09

This file tracks what has been added to the datapack, what is still being worked on, and what remains to be tested.

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

## In progress

- [ ] Vein mining.
  - Ore mining should only chain through connected blocks of the exact same ore type.
  - Different ore types must never be included in the same chain.
  - Tree mining should chain connected logs only when the player is using an axe.
  - A block limit is planned to prevent excessively large chains.

## Not yet verified

- [ ] Confirm datapack compatibility with the target Minecraft server version (26.3).
- [ ] Test every custom recipe in-game.
- [ ] Test ore generation in newly generated chunks.
- [ ] Test vein mining in-game once implemented.
- [ ] Confirm the datapack loads without errors on the Aternos server.

## Notes

- Adding a world-generation change does not alter chunks that have already been generated.
- The ore-generation adjustments are intended settings and have not been confirmed by measured in-game generation tests.
- Vein mining is **not implemented yet**. Its requirements are recorded above so the implementation can be checked against them.
- This report will be updated as features are added and tested.
