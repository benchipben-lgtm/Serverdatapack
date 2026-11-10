# Server Datapack (Minecraft Java 26.3)

A datapack for an Aternos Java server. World-generation changes affect newly generated chunks only.

## Implemented in this update

- **Diamonds:** one or two cluster placement attempts per chunk, distributed uniformly from Y=-64 through Y=32. Each attempt uses a custom ore feature with size 9, targeting both stone and deepslate.
- The other vanilla diamond placement routes (large, medium, and buried) are disabled so they do not add extra clusters.

**Important generation note:** Minecraft's ore feature size is a maximum placement size, not a guaranteed exact number of blocks. The datapack targets 1–2 attempts per chunk and a maximum cluster size of 9; terrain, caves, and replacement rules can make an individual cluster smaller. In-game testing is still required.

## Existing custom recipes

### Trident recipe

```text
SDS
 T
 P
```

- S = Prismarine Shard
- D = Diamond Block
- T = Tide Armor Trim Smithing Template
- P = Sponge

Crafts 1 Trident.

### Heavy Core recipe

```text
 E
INI
 D
```

- E = Ender Eye
- I = Iron Block
- N = Netherite Block
- D = Diamond Block

Crafts 1 Heavy Core.

## Ancient debris

The repository includes a large ancient-debris placement override intended to increase generation between Y=8 and Y=26. This still needs a full Java 26.3 load and in-game verification.

## Vein mining and tree felling

This project uses the companion **VeinBreaker** datapack for connected-ore mining and axe-based tree felling. Install it alongside this datapack in the same world's `datapacks` folder. Follow [VEIN_MINER.md](VEIN_MINER.md) for the official download, Aternos installation steps, and toggle commands. The companion datapack is maintained separately and is not bundled into this repository.

## World design and spawners

See [WORLD_DESIGN.md](WORLD_DESIGN.md) for the full Overworld, Nether, mob, and spawner plan, plus implementation limitations and progress.

## Install

Download this repository as a ZIP and place it in the world's `datapacks` folder. Also install the VeinBreaker companion ZIP as described in [VEIN_MINER.md](VEIN_MINER.md). Restart the server or run `/reload`, then check `/datapack list`.

Ore and structure-generation changes apply to newly generated chunks only. Existing chunks will not be retroactively regenerated.
