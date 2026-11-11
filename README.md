# Server Datapack — Minecraft Java 26.3

This pack targets Java 26.3 (data pack format 121.0). Install the folder containing `pack.mcmeta` and `data/` into the world's `datapacks/` folder. Enable it before generating the world. Terrain, biome, ore, and structure changes affect newly generated chunks; a fresh world is recommended.

## Overworld

- The cavern floor is shaped around Y=-46 with broad natural variation, leaving a solid buffer above the usual Y=-54 lava layer.
- The roof uses a separate broad terrain-noise boundary around Y=-10, with several-block height variation rather than a flat cutoff.
- Aquifer exclusion follows the same floor/roof boundaries and is positive only inside the intended cavern volume.
- Large 3D noise formations add occasional broad cave walls and solid sections.
- A separate low-frequency noise mask adds rare broad plateaus roughly 20 blocks tall, with irregular edges.
- The 26.3 beardifier is applied once at the final density root so structure terrain adaptation also affects the custom cavern branch.
- Ancient Cities use 12-chunk placement spacing, are allowed in Overworld biomes, start at Y=-27, and use 16-block dimension padding to keep pieces away from the bedrock boundary.
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
- Circularity of the plateaus and the visual density of walls depend on the noise field and need an in-game worldgen check.
- Silk Touch spawner drops and truly unbreakable Blaze spawners are not implemented in this datapack yet.
- JSON syntax and registry references can be statically checked, but the pack has not yet been loaded by a Minecraft 26.3 server in this environment.
