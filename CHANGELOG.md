# Changelog

## 1.0.1 - Existing worlds listed as Riverheim Hybrid

* Hybrid worlds created before 1.0.0 were listed as plain **Riverheim** in Worldhalla's world list, although they still generated with their vanilla core. When loaded, they are now listed as **Riverheim Hybrid**, and their saved settings move from `BepInEx/config/RiverheimHybrid/worlds/` into the world on its next save. Their terrain, biomes, and locations are unchanged.
* Once moved, these worlds get the same protection as new ones: Worldhalla refuses to load them without the companion and refuses players without the matching version.
* Plain Riverheim worlds stay plain. Update the companion on the server and every client.

## 1.0.0 - Riverheim Hybrid world generator

Update the companion on the server and every client. Requires Riverheim 1.3.1 and Worldhalla 1.0.0, as since 0.2.1.

* Adds **Riverheim Hybrid** to Worldhalla's world-creation window. Choose it to create a Riverheim world with a vanilla core; plain Riverheim now creates plain Riverheim worlds.
* Every setting can be chosen when creating the world: Riverheim preset, generation (Hybrid v2 or legacy), vanilla radius, edge variation and wavelength, biome offset, transition width, margins, and preservation options. New worlds default to Hybrid v2.
* Worldhalla's preview shows the world with its vanilla core.
* A world's settings are saved in the world and sent to players by Worldhalla, which refuses players without the matching companion. A Riverheim Hybrid world cannot be opened without the companion, so it can no longer be generated as plain Riverheim by mistake.
* Dedicated servers create a Riverheim Hybrid world with `-wh guid sterbenden.riverheim.hybrid`, optionally with `-wh settings "..."`.
* The companion's configuration now holds the defaults offered for new Riverheim Hybrid worlds, in a new section. Worlds created with earlier versions keep their saved settings and generate exactly as before.

## 0.2.1 - Riverheim 1.3.1 and Worldhalla

Requires **Riverheim 1.3.1** and **Worldhalla 1.0.0**. Update the companion, Riverheim, and Worldhalla together on the server and every client.

* Supports Riverheim 1.3.1, which now runs as a Worldhalla world generator. The companion detects Riverheim worlds through Worldhalla and works with worlds created in Worldhalla's world-creation window or on a dedicated server started with `-wh guid dev.gurebu.riverheim`.
* Existing worlds keep working: Worldhalla converts Riverheim 1.2.1 worlds on first load, and the companion keeps their saved settings and Hybrid v2 readiness records. Terrain, biomes, and locations generate exactly as with 0.1.4 and Riverheim 1.2.1.
* Vanilla worlds and worlds made with other Worldhalla generators no longer receive a companion settings file.
* Worldhalla's world preview is no longer affected by the companion's settings from a previously loaded world.
* With an unsupported Riverheim or Worldhalla version, or without Worldhalla, the companion stays disabled and refuses to load worlds that use its vanilla core.
* Outside the vanilla core, Worldhalla rounds Riverheim's forest density very slightly differently from Riverheim 1.2.1. This can at most shift an individual plant in areas that have not been explored yet; explored areas and the vanilla core are unaffected.
* Works on Valheim 1.0.20 and 1.0.21.
* This is the first public release of this update; version 0.2.0 was not published.

## 0.1.4 - Game update compatibility

* Removed the exact Valheim 1.0.20 requirement that prevented Hybrid v2 worlds from loading on newer game versions, including 1.0.21.
* Server and clients must install the same companion version. Saved world generation settings and the Riverheim 1.2.1 requirement are unchanged.

## 0.1.3

* Expanded the Hybrid v2 release notes and retained the complete release history.

## 0.1.2 - Corrected release metadata

- Retain the complete historical changelog alongside the Hybrid v2 release notes.

## 0.1.1

Major update. New worlds can use Hybrid v2, while existing worlds keep their saved generation settings. The companion and the generator must be updated together when using v2.

* Added a 1,350-metre vanilla core with a 900-metre transition into Riverheim terrain and a gently varying edge.
* Vanilla biome sectors and protected vanilla locations are replayed in the core, while eligible Riverheim locations are preserved beyond the transition.
* Added deterministic location reconciliation and bounded repairs for required location variants, with clear diagnostics when a world cannot be completed safely.
* Terrain blends now follow the game's four-corner height interpolation, avoiding the sharp edge changes seen in earlier transitions.
* Added versioned per-world settings, identity fingerprints, Riverheim profile checks, and readiness records so generated worlds cannot silently change after creation.
* A world that fails its v2 location or identity checks cannot materialize zones, save, or admit incompatible multiplayer peers.
* Added strict client/server settings synchronization and compatibility errors for incomplete or mismatched installations.
* Separated v2 biome and terrain caches from legacy data to prevent incompatible cached results from being reused.
* Added matching native and browser generator support for v2 terrain, biomes, and location reconciliation.

## 0.1.0

- Preserve a vanilla core around the center of new Riverheim worlds, with a blended transition into Riverheim terrain.
- Preserve vanilla biomes, locations, and vegetation in protected areas.
- Save generation settings separately for each world and synchronize the host's settings to clients.
- Leave existing worlds unchanged by default.
- Require matching companion versions on the server and clients and Riverheim 1.2.1.


