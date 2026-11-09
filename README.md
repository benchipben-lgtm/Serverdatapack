# Ore Tweaks (Minecraft Java 26.3)

A datapack for an Aternos Java server.

## Changes
- Diamond ore generation reduced (target: about 60% fewer than vanilla).
- Ancient debris generation increased: 6 placement attempts, concentrated between Y=8 and Y=26, with large-feature size raised to 6. Actual vein block counts can still vary and are not guaranteed to be exactly 2–6.
- Small Nether lava springs reduced; lava lakes are unchanged.
- Adds a shaped Trident recipe.

## Trident recipe
Pattern (top to bottom):

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

## Vein mining and tree felling
This project uses the companion **VeinBreaker** datapack for connected-ore mining and axe-based tree felling. Install it alongside this datapack in the same world's `datapacks` folder. Follow [VEIN_MINER.md](VEIN_MINER.md) for the official download, Aternos installation steps, and toggle commands. The companion datapack is maintained separately and is not bundled into this repository.

## Install
Download this repository as a ZIP and place it in the world's `datapacks` folder. Also install the VeinBreaker companion ZIP as described in [VEIN_MINER.md](VEIN_MINER.md). Restart the server or run `/reload`, then check `/datapack list`. Ore-generation changes apply to newly generated chunks only.

Note: Actual ore yields vary by terrain, biome, and placement rules. The stated multipliers are generation-attempt targets, not guaranteed per-chunk block counts.
