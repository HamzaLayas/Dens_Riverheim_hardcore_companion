# Den’s Riverheim Hardcore Companion

A Valheim companion mod by **SterbenDen** for **Riverheim 1.2.1**. Version 0.1.4 removes the exact game-version restriction, allowing use on Valheim 1.0.21.

Keep the terrain around the center of a new world faithful to its vanilla seed while Riverheim shapes the land farther out. The default vanilla core extends at least 1,350 metres from the center, with a gently varying edge and a 300-metre transition into Riverheim terrain. Protected areas preserve vanilla biomes, locations, and vegetation.

## Installation

Install the same version on the dedicated server and every player's PC. Back up your worlds before changing world-generation mods.

1. Stop the server and close Valheim.
2. Install [BepInExPack Valheim](https://valheim.hexium.gg/mods/denikson/BepInExPack_Valheim) and **Riverheim 1.2.1**.
3. Download the installer ZIP from [Releases](https://github.com/HamzaLayas/Dens_Riverheim_hardcore_companion/releases) and extract it into the Valheim folder on the server and every client.
4. Keep only one copy of `RiverheimHybrid.dll` under `BepInEx/plugins/`. The installer places it in `BepInEx/plugins/RiverheimHybrid/`.
5. Start a new world to use the vanilla core. Worlds created before installing the companion remain unchanged by default.

The installer contains only this companion's DLL. Install BepInEx and Riverheim separately. GitHub's automatic source archives contain the player guide and icon; use the installer ZIP to install the mod.

## World settings

The default settings are generated in `BepInEx/config/sterbenden.riverheim.hybrid.cfg`. Change these before creating a new world to choose its vanilla radius, edge variation, transition width, and preservation options.

Each world's settings are saved separately in `BepInEx/config/RiverheimHybrid/worlds/<name>_<uid>.cfg`. Changing the defaults does not change settings already saved for a world. Editing a world's generation settings after exploring it can create terrain seams; keep a backup and use a new world for a different layout.

The host or server sends the world's settings to clients. A server using the companion refuses clients without the matching version. Existing worlds receive disabled settings, preserving their previous generation behavior.

## Compatibility and updates

This version supports exactly **Riverheim 1.2.1**. With another Riverheim version, the companion logs an error and stays disabled. Use matching versions on the server and clients.

Back up your world and configuration, stop the server and clients, and replace the companion DLL when updating. Preserve your configuration and per-world settings. Mods that change terrain, biomes, locations, vegetation, or world generation may conflict.

[Downloads](https://github.com/HamzaLayas/Dens_Riverheim_hardcore_companion/releases) · [Report a problem](https://github.com/HamzaLayas/Dens_Riverheim_hardcore_companion/issues)

## Artwork

The Cartography Table icon is Valheim game artwork owned by Iron Gate AB, reproduced from [Jötunn’s exported game assets](https://github.com/Valheim-Modding/Jotunn/blob/f4bb47121f1685712b2bcf1279b61fe6de996074/JotunnLib/Documentation/images/pieces/piece_cartographytable.png). This is a community mod and is not affiliated with Iron Gate AB.
