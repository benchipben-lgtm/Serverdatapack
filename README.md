# Server Datapack — Minecraft Java 26.3

This pack targets Java 26.3 (data pack format 121.0). Install the folder containing `pack.mcmeta` and `data/` into the world's `datapacks/` folder. Enable it before generating the world. Terrain, biome, ore, and structure changes affect newly generated chunks; a fresh world is recommended.

## Overworld

- A large cavern band is carved from roughly Y=-59 up to an uneven roof around Y=-10.
- Aquifer fluids are suppressed inside that cavern band so it stays dry; the normal bedrock floor is left intact.
- Ancient City structures use roughly 12-chunk placement spacing and may start between Y=-52 and Y=-35. They are allowed in all Overworld biomes, rather than only Deep Dark.
- Villages use 23-chunk spacing.
- Trial Chambers use 23-chunk spacing (about 119% more placement density than the vanilla 34-chunk spacing).
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

- Deep Dark biome frequency itself remains vanilla. The normal Overworld biome distribution is hardcoded; changing it safely requires a custom world preset with a full replacement climate table. The pack instead allows Ancient Cities across Overworld biomes.
- Silk Touch spawner drops and truly unbreakable Blaze spawners are not implemented in this datapack yet.
- The files have been checked for valid JSON and reviewed against the 26.3 data format, but have not been loaded by a Minecraft 26.3 server in this environment.
