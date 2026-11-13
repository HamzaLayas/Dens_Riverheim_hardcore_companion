# Changelog

## 1.0.3 - Worldhalla 1.0.1

* Works with **Worldhalla 1.0.1**. With 1.0.2, your Riverheim Hybrid worlds won't open once Worldhalla updates to 1.0.1, so update the companion and Worldhalla together on the server and every client.
* Hosts that can't add command-line options can now create a Riverheim Hybrid world from Worldhalla's config. Set `Generator = sterbenden.riverheim.hybrid` in the `[World creation]` section of `BepInEx/config/dev.gurebu.worldhalla.cfg`, and optionally `Settings`, for example `generation 2 radius 1350`.
* On a PC, the same config makes **Riverheim Hybrid** the starting choice in the world-creation window.
* Your worlds generate exactly as before.

## 1.0.2 - Now on Hexium

* Now available on Hexium as well as GitHub.
* Includes the 1.0.1 fix: worlds you made with a vanilla core before 1.0.0 show up as **Riverheim Hybrid** again.
* Install the same version on the server and every client.

## 1.0.1 - Older worlds show as Riverheim Hybrid

* Worlds you made with a vanilla core before 1.0.0 were shown as plain **Riverheim** in the world list. They still had their vanilla core, only the label was wrong. They now show as **Riverheim Hybrid**.
* Load and save each of those worlds once. After that the world remembers its own settings, so keep `BepInEx/config/RiverheimHybrid/worlds/` until you have done that.
* Nothing about the terrain changes.

## 1.0.0 - Riverheim Hybrid in the world list

* New **Riverheim Hybrid** option when creating a world. Pick it to get a vanilla core; picking **Riverheim** now gives you a plain Riverheim world.
* All settings are in the world-creation window: Riverheim preset, Hybrid v2 or legacy, vanilla radius, edge shape, transition width, and which vanilla content to keep. New worlds use Hybrid v2.
* The world preview shows the vanilla core.
* Each world keeps its own settings, and players joining a server get them automatically. Players without the companion can't join a Riverheim Hybrid world.
* Dedicated servers: start with `-wh guid sterbenden.riverheim.hybrid` to create a Riverheim Hybrid world.
* Your existing worlds generate exactly as before.

## 0.2.1 - Riverheim 1.3.1

* Works with **Riverheim 1.3.1**, which needs **Worldhalla 1.0.0**. Update the companion, Riverheim and Worldhalla together on the server and every client.
* Your existing worlds keep working and generate exactly as before.
* If Riverheim or Worldhalla is the wrong version, the companion won't load your vanilla-core worlds rather than letting them generate without it.
* Works on Valheim 1.0.20 and 1.0.21.

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


