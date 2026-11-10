# Datapack Progress Report

Last updated: 2026-11-10

This file tracks what has been added, what is being worked on, and what still needs testing.

## Completed / added to repository

- [x] Initial datapack structure and README.
- [x] Custom ore-generation changes added to the datapack.
- [x] Diamond generation reworked to target 1–2 cluster attempts per chunk, from Y=-64 through Y=32.
- [x] Disabled the extra vanilla large, medium, and buried diamond placement routes so they do not stack on top of the new cluster route.
- [x] Added a custom diamond ore feature with size 9, targeting stone and deepslate ore-replaceable blocks.
- [x] Ancient debris large-vein placement override and feature file are present (Java 26.3 format/load status still needs review).
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
- [x] Added [WORLD_DESIGN.md](WORLD_DESIGN.md) with the full world-generation and spawner specification.

## Vein miner — solution identified

**Status: INSTALLATION GUIDE ADDED — COMPANION ZIP STILL NEEDS SERVER INSTALLATION**

A separate Minecraft Java 26.3 datapack, [VeinBreaker by lays24mc](https://www.curseforge.com/minecraft/data-packs/veinbreaker), advertises the requested mechanics:

- Connected ore veins are mined by same ore type.
- Tree felling activates when using an axe.
- Fortune, Silk Touch, Unbreaking, and tool durability are supported.
- Players can toggle tree felling and ore vein mining independently with trigger commands.
- The 1.1 release notes a 256-block reach; earlier release listed a 32-block limit.

**Server software decision:** Keep the server on Vanilla Java 26.3. A plugin server is not necessary for the vein-mining solution.

**Integration status:** The companion ZIP is not bundled in this repository; upload it separately into the same world's `datapacks` folder. Do not mark vein mining complete until it is enabled and tested in-game.

## Not yet implemented

- [ ] Greatly increase dungeon generation.
- [ ] Increase amethyst geode generation.
- [ ] Increase village generation by 120%.
- [ ] Increase Nether fortress generation by 120%.
- [ ] Create the huge hollow underground layer below Y=-34, with Ancient Cities throughout and large connecting caverns where feasible.
- [ ] Disable small Nether lava pools while preserving large lava lakes.
- [ ] Increase fortress wither skeleton spawns; add rare Soul Sand Valley spawns.
- [ ] Increase wither skeleton skull drops and add rare diamond drops.
- [ ] Increase undead aggression.
- [ ] Increase Enderman spawns in Warped Forests.
- [ ] Add Haste I/II/III potion recipes and Redstone Block duration extension.
- [ ] Add faster furnaces.
- [ ] Add golden-apple repeat-consumption penalties.
- [ ] Implement Silk Touch spawner pickup with the Blaze Spawner exception, after selecting a technically viable implementation.
- [ ] Add the remaining requested combat and command changes (tracked separately from world generation).

## Spawner limitation to resolve

A loot-table change can make a spawner drop when mined with Silk Touch, but a vanilla datapack does not have a reliable block-break hook that can stop only Blaze Spawners from being broken. The desired rule is that ordinary spawners are Silk Touch-mineable while Blaze Spawners remain unbreakable. Do not mark this feature complete or install a generic spawner-drop override until the Blaze exception can be enforced without breaking the rule.

## Testing still required

- [ ] Confirm the pack loads cleanly on a real Java 26.3 server / Aternos.
- [ ] Verify diamond cluster attempts, distribution, and actual block counts in newly generated chunks.
- [ ] Verify diamond generation is not duplicated by another vanilla placed-feature route.
- [ ] Review the ancient-debris feature against the Java 26.3 worldgen registry format.
- [ ] Test every custom recipe in-game.
- [ ] Upload/install the VeinBreaker ZIP on Aternos and verify exact ore matching.
- [ ] Verify tree felling requires an axe.
- [ ] Confirm all datapacks load without errors on Aternos.

## Notes

- World-generation changes affect newly generated chunks, not chunks that already exist.
- Ore-feature size is a maximum, not a guaranteed exact block count. The diamond cluster size 9 therefore means up to 9 ore blocks per successful placement attempt, not a hard guarantee of 6–9.
- Placement attempts can fail where terrain does not provide valid replacement blocks, so 1–2 is the target attempt count, not a guarantee that every chunk will contain 1–2 visible clusters.
- This report distinguishes repository changes from features that are only planned or still require in-game testing.
