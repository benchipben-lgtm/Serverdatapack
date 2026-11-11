# Server Datapack — Minecraft Java 26.3

This pack targets Java 26.3 (data pack format 121.0). Install the folder containing `pack.mcmeta` and `data/` into the world's `datapacks/` folder. Enable it before generating the world. Terrain, biome, ore, and structure changes affect newly generated chunks; a fresh world is recommended.

## Overworld

- The custom cavern system begins above the bedrock region. Its lower boundary is now a noise-shaped solid floor around Y=-50, intended to keep the usual Y=-54 lava layer beneath the playable cavern.
- The cavern roof is shaped by broad Overworld noise fields instead of a single flat Y=-10 cutoff. Its height varies by location and can extend somewhat above Y=-10.
- Aquifers are excluded from the custom cavern band through Y=15 so the hollow area should remain dry.
- Ancient Cities use 12-chunk placement spacing, are allowed in Overworld biomes, and now start at Y=-27 with dimension padding to keep pieces away from the world bottom.
- Trial Chambers now use the same 12-chunk spacing and 1-chunk separation as Ancient Cities, giving them the same placement-grid frequency. Their biome eligibility still differs.
- Villages use 23-chunk spacing.
- Monster rooms and deep monster rooms are increased to 22 and 9 placement attempts respectively.
- Amethyst geodes use rarity 11 instead of vanilla rarity 24.
- Diamonds use size-9 clusters with a one-in-four-chunks placement chance. Individual clusters can contain fewer than nine blocks because ore replacement rules still apply.

## Nether

- Nether Fortresses use 18-chunk spacing instead of vanilla 27 (about 125% more placement density).
- Wither Skeleton weight in fortress pieces is doubled.
- Rare Wither Skeleton spawns are added to Soul Sand Valleys.
- Warped Forest Enderman spawn capacity is increased from 0.12 to 0.30.
- Small Nether spring features are disabled. Larger lava lakes are not overridden.

## Recipes

- Heavy Core: Eye of Ender above a Netherite Block, Iron Blocks on either side, and a Diamond Block below.
- Trident: Prismarine Shards across the top, a Diamond Block in the upper middle, Tide Armor Trim in the center, and a Sponge at the bottom.

## Known limitations

- Deep Dark biome frequency itself remains vanilla. The pack instead allows Ancient Cities across Overworld biomes.
- Large circular plateaus and giant internal cave walls are not implemented yet; they are a separate terrain-shaping pass after the floor, roof, fluid, and structure-height fixes are tested.
- Silk Touch spawner drops and truly unbreakable Blaze spawners are not implemented in this datapack yet.
- JSON syntax checks do not replace loading the pack in a Minecraft 26.3 server. This revision has not been runtime-tested in Minecraft.
