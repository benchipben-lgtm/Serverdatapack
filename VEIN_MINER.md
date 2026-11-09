# Vein mining add-on (Minecraft Java 26.3)

This project uses **VeinBreaker 1.1 by lays24mc** as a companion datapack for vein mining and tree felling.

The companion pack is maintained separately, so this repository links to its official release instead of copying or modifying the author's files.

## Official download

- [VeinBreaker 1.1 — Minecraft Java 26.3 (CurseForge file page)](https://www.curseforge.com/minecraft/data-packs/veinbreaker/files/9289200)
- [VeinBreaker project page](https://www.curseforge.com/minecraft/data-packs/veinbreaker)

## Install on Aternos

1. Download the 26.3 ZIP from the official file page above.
2. In Aternos, open **Files** and navigate to your world's `datapacks` folder.
3. Upload the VeinBreaker ZIP there. Keep it as a ZIP; do not extract it.
4. Restart the server, or run `/reload`.
5. Run `/datapack list` in-game and confirm VeinBreaker appears as enabled.

Keep the existing Serverdatapack installed too. The two packs are separate and should be installed side by side in the same world's `datapacks` folder.

## Controls

VeinBreaker documents these player commands:

- `/trigger veinbreaker_axe` — toggle tree felling.
- `/trigger veinbreaker_pickaxe` — toggle ore vein mining.

Both features are enabled by default according to the project page.

## Behavior described by the author

- Ore mining follows connected blocks of the same ore type; different ore types are not mixed.
- Tree felling requires an axe.
- Fortune, Silk Touch, Unbreaking, and tool durability are supported.
- Release 1.1 increases the chain reach from 32 to 256 blocks.

These behaviors are based on the author's release description and still need to be tested on this Aternos server.

## Important

This file is an installation guide, not the VeinBreaker datapack itself. The companion ZIP must be downloaded from the official release page and uploaded to the server separately. Do not mark the feature as tested until it works in-game.
