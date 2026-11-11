# Server Datapack — Minecraft Java 26.3

This pack targets Java 26.3 (data pack format 121.0). Install the folder containing `pack.mcmeta` and `data/` into the world's `datapacks/` folder. Enable it before generating the world. Terrain, biome, ore, and structure changes affect newly generated chunks; a fresh world is recommended.

## Overworld

- The cavern floor uses a plains-like profile centered near Y=-46, with smooth height variation of up to about 3 blocks above or below the center. A tighter horizontal noise scale makes the rises and dips more visible. Aquifer exclusion follows the exact same floor shape.
- The cavern roof boundary is centered near Y=15, with broad terrain-noise variation targeting roughly Y=9–21 rather than a flat cutoff.
- Aquifer exclusion follows the same irregular floor and roof boundaries and is positive only inside the intended cavern volume.
- Thin, winding 2D noise contours create vertical cave-wall sheets rather than oval columns. Their lower edges vary around Y=-4 and their upper edges around Y=12, giving both ends a curved, uneven outline while leaving the lower Ancient City band clear.
- A sparse broad mask creates raised cliff-like plateaus with irregular edges and uneven tops, roughly 11–15 blocks above the rolling floor.
- The cavern interior is now forced open air throughout the space between the floor and roof, except where the custom wall and plateau masks deliberately add solid terrain. This prevents ordinary cave-cheese density from leaving random solid masses that can bury Ancient Cities. The 26.3 beardifier remains applied once at the final density root.
- Ancient Cities use 12-chunk placement spacing and are allowed in Overworld biomes. They now start at Y=-20 and use `terrain_adaptation: none` so the structure does not pull surrounding cavern density into its footprint and get buried by the custom floor. Their structure definition follows the Java 26.3 schema (no unsupported `dimension_padding` field).
- Trial Chambers use the same 12-chunk spacing, 1-chunk separation, and Overworld biome eligibility as Ancient Cities. Their full vanilla pool aliases and other structure settings are retained; their start-height range is raised to Y=-30 through -18, with 16-block dimension padding.
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

- Deep Dark biome frequency itself remains vanilla. Ancient Cities are allowed in all Overworld biomes.
- Circularity of the plateaus, the visual density of walls, and the final cavern profile still need an in-game worldgen check.
- Silk Touch spawner drops and truly unbreakable Blaze spawners are not implemented in this datapack yet.
- JSON syntax can be checked here, but the pack still needs to be loaded by a Minecraft 26.3 server to confirm registry decoding and generated terrain.
