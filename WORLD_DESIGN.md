# World Design and Spawner Specification

Target: Minecraft Java 26.3 on Aternos.

This document is the current agreed design. Checkboxes distinguish features already committed from features still planned.

## Overworld

- [ ] **Ancient City underground layer**
  - Below Y=-34, create a huge hollow underground region.
  - Generate Ancient Cities throughout it.
  - Cities do not need to connect seamlessly; large caverns and air pockets between cities are acceptable.
  - Aim for the atmosphere of one enormous underground civilization.
  - Vanilla datapack structure placement cannot promise a continuous hollow layer or a city in every chunk. The implementation must be tested in a disposable world before being treated as complete.
- [ ] **Dungeons:** greatly increase dungeon generation.
- [ ] **Amethyst geodes:** increase generation rates.
- [ ] **Villages:** increase generation by 120%.
- [x] **Diamonds:** target 1–2 cluster placement attempts per chunk.
  - Height range: Y=-64 through Y=32, distributed uniformly.
  - Custom ore feature size: 9.
  - Both stone and deepslate diamond ore are supported.
  - Extra vanilla large, medium, and buried diamond placement routes are disabled.
  - The ore feature's size is a maximum, not a guaranteed count; actual clusters can be smaller than 6–9.

## Nether

- [ ] **Nether Fortresses:** increase generation by 120%.
- [ ] **Small lava pools:** disable small Nether lava pools.
- [ ] **Large lava lakes:** leave unchanged.

## Mob generation and drops

- [ ] Increase wither skeleton spawn rates inside Nether Fortresses.
- [ ] Allow rare wither skeleton spawns in Soul Sand Valleys.
- [ ] Increase wither skeleton skull drop rates.
- [ ] Give wither skeletons a rare diamond drop.
- [ ] Increase undead aggression.
- [ ] Increase Enderman spawn rates in Warped Forests.

## Spawner rules

- [ ] All ordinary spawners should be obtainable with Silk Touch.
- [ ] Blaze Spawners must remain unbreakable and must never be collected.

**Technical note:** A datapack can alter spawner loot, but vanilla datapacks do not provide a dependable way to cancel the block break only when the spawner contains a Blaze. A generic Silk Touch spawner-drop table would violate the Blaze exception. Keep this feature pending until a compatible implementation is chosen and tested.

## World-generation behavior

- These changes affect newly generated chunks only.
- Existing chunks do not regenerate automatically.
- Generation multipliers are targets for placement attempts, not guarantees of a precise number of structures in every chunk.
