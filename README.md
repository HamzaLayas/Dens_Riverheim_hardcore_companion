# Den’s Riverheim Hardcore Companion

A Valheim companion mod by **SterbenDen** for **Riverheim 1.3.1** on **Worldhalla 1.0.0**. It adds a **Riverheim Hybrid** world generator to Worldhalla's world-creation window, and works on Valheim 1.0.20 and 1.0.21.

A Riverheim Hybrid world keeps the land around the center faithful to its vanilla seed while Riverheim shapes the world farther out. By default the vanilla core extends at least 1,350 metres from the center, with a gently varying edge and a 900-metre transition into Riverheim terrain (300 metres for legacy worlds). Protected areas preserve vanilla biomes, locations, and vegetation.

## Installation

Install the same version on the dedicated server and every player's PC. Back up your worlds before changing world-generation mods.

1. Stop the server and close Valheim.
2. Install [BepInExPack Valheim](https://valheim.hexium.gg/mods/denikson/BepInExPack_Valheim), [Worldhalla 1.0.0](https://thunderstore.io/c/valheim/p/Gurebu/Worldhalla/) and [Riverheim 1.3.1](https://thunderstore.io/c/valheim/p/Gurebu/Riverheim/). Worldhalla and Riverheim are published on Thunderstore; if your mod manager cannot find them (for example on Hexium), install them from there.
3. Download the installer ZIP from [Releases](https://github.com/HamzaLayas/Dens_Riverheim_hardcore_companion/releases) and extract it into the Valheim folder on the server and every client.
4. Keep only one copy of `RiverheimHybrid.dll` under `BepInEx/plugins/`. The installer places it in `BepInEx/plugins/RiverheimHybrid/`.

The installer contains only this companion's DLL. Install BepInEx, Worldhalla, and Riverheim separately. GitHub's automatic source archives contain the player guide and icon; use the installer ZIP to install the mod.

## Creating a world

In the world-creation window, choose **Riverheim Hybrid** as the world generator. Its settings button shows the Riverheim preset and every companion setting: generation (Hybrid v2 or legacy), vanilla radius, edge variation, transition width, and preservation options. The preview shows the world with its vanilla core.

On a dedicated server, create the world with:

```
valheim_server -world MyWorld -wh guid sterbenden.riverheim.hybrid
```

Settings not given use the defaults described below. To choose them on the command line, add for example `-wh settings "preset builtin.amur generation 2 radius 1350 edge-variation 150"`. These options only apply when the world is created.

Choosing plain **Riverheim** creates a plain Riverheim world without a vanilla core.

## World settings

A world's settings are saved in the world itself when it is created, and the server sends them to clients. They cannot be changed later, because that would change the terrain; use a new world for a different layout.

The values pre-filled in the world-creation window, and used by a dedicated server for settings it was not given, come from `BepInEx/config/sterbenden.riverheim.hybrid.cfg`.

## Compatibility and updates

This version supports exactly **Riverheim 1.3.1** with **Worldhalla 1.0.0**, and the server and every client need the same companion version; Worldhalla refuses players who don't have it. A Riverheim Hybrid world cannot be opened without the companion, so it is never generated as plain Riverheim by mistake.

**Updating from earlier versions:** back up your worlds and configuration, stop the server and clients, then update the companion, Riverheim, and Worldhalla together everywhere. Worlds made with earlier versions keep their saved settings in `BepInEx/config/RiverheimHybrid/worlds/` and generate exactly as before; keep that folder. Worldhalla converts Riverheim 1.2.1 worlds when they are first loaded, and Riverheim 1.2.1 cannot open a world after Worldhalla has saved it, so keep the backup if you may need to go back.

Mods that change terrain, biomes, locations, vegetation, or world generation may conflict. Worldhalla's own compatibility notes also apply; for example, it is incompatible with Better Continents and with mods that replace the world-creation window.

[Downloads](https://github.com/HamzaLayas/Dens_Riverheim_hardcore_companion/releases) · [Report a problem](https://github.com/HamzaLayas/Dens_Riverheim_hardcore_companion/issues)

## Artwork

The Cartography Table icon is Valheim game artwork owned by Iron Gate AB, reproduced from [Jötunn’s exported game assets](https://github.com/Valheim-Modding/Jotunn/blob/f4bb47121f1685712b2bcf1279b61fe6de996074/JotunnLib/Documentation/images/pieces/piece_cartographytable.png). This is a community mod and is not affiliated with Iron Gate AB.
