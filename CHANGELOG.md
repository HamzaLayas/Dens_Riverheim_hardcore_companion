# Changelog

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


