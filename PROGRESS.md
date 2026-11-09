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

## Vein miner — solution identified

**Status: COMPATIBLE SOLUTION FOUND — NOT YET ADDED TO THIS REPOSITORY**

A separate Minecraft Java 26.3 datapack, [VeinBreaker by lays24mc](https://www.curseforge.com/minecraft/data-packs/veinbreaker), advertises the requested mechanics:

- Connected ore veins are mined by same ore type.
- Tree felling activates when using an axe.
- Fortune, Silk Touch, Unbreaking, and tool durability are supported.
- Players can toggle tree felling and ore vein mining independently with trigger commands.
- The 1.1 release notes a 256-block reach; earlier release listed a 32-block limit.

**Server software decision:** Keep the server on Vanilla Java 26.3. A plugin server is not necessary for this solution.

**Integration status:** The external datapack has not been merged into this repository. It must be installed as its own datapack alongside this one unless its files are deliberately merged and checked for namespace/function conflicts. Do not mark vein mining complete until that integration and an in-game test are done.

## Not yet verified

- [ ] Confirm the current custom datapack's pack metadata is correct for Java 26.3.
- [ ] Test every custom recipe in-game.
- [ ] Test ore generation in newly generated chunks.
- [ ] Add or install VeinBreaker and verify exact ore matching.
- [ ] Verify tree felling requires an axe.
- [ ] Verify the chain limit and tool durability behavior in-game.
- [ ] Confirm all datapacks load without errors on Aternos.

## Notes

- World-generation changes affect newly generated chunks, not chunks that already exist.
- Ore-generation adjustments are intended settings and have not been confirmed by measured in-game generation tests.
- This report distinguishes features present in this repository from separate datapacks that have only been identified as compatible candidates.
