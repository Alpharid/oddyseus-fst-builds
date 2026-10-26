# Oddyseus : F.S.T.

![Oddyseus : F.S.T.](https://raw.githubusercontent.com/Alpharid/ACH/main/web/assets/filiales/oddyseus-1.webp)

You are the **F.S.T. (Fail-Safe Taskforce)**, woken as a last resort aboard the **Oddyseus**, a colossal
colony ark drifting blind. Its AI, **A.R.G.O.S.**, has lost its memory and the cryo-sleeping colonists'
life support is failing. Salvage everything that isn't vital, turn it into raw matter, fabricate parts,
repair the ship… and find out what really happened.

A first-person zero-gravity immersive sim, **1 to 8 players in co-op** (Godot 4.7).

This repository is the game's **public distribution channel**: it only carries binaries, published as
GitHub Releases. The source code is private.

## Features

- A procedurally generated 740 m station: luxury lounges, casino, cryo bay, bridge, spacewalks
  outside the hull.
- Zero-G, magnetic boots to walk on walls and ceilings, a suit to manage (power, oxygen, radiation,
  heat, cold).
- Cutting, disassembly into elements, Poly-Cubes, component fabrication, welding, power grid,
  room restoration.
- Atmosphere simulated room by room (breaches, leaks, emergency bulkheads) and a fully dismantlable ship.
- Asteroid fields, radiation belts, hull impacts, a colony vitality that keeps declining.
- An investigation, a final vote and several endings; text and voice in English and French.
- 4 complementary classes: C.E.U (engineer), R.C.U (recovery), H.A.U (hazard), B.O.U (recon).

## Status

Alpha: the game's first phase (regaining control of the ship) is playable end to end.
Latest builds: **PROD 0.2.0** and **UNSTABLE 0.4.0** (pressure and ship dismantling).

## Play

1. Download
   **[`OddyseusLauncher.exe`](https://github.com/Alpharid/oddyseus-fst-builds/releases/tag/launcher)** once
   and keep it. Windows SmartScreen may warn because the exe is not code-signed: *More info* >
   *Run anyway*.
2. Start it, pick **PROD** (stable) or **UNSTABLE** (newest features, may break), then *Play*.
   The launcher downloads and verifies the build, updates itself and the game: it never needs to be
   re-sent.
3. In the game: *Host a mission* (you can play alone) or *Join a mission* (paste the host's link).
   Everybody in a game must have **the same build** (same channel, same version): the game refuses the
   connection otherwise.

## System requirements

- Windows 10/11 64-bit.
- Vulkan capable GPU.

## Releases

| tag | what |
|---|---|
| `launcher` | the launcher (`OddyseusLauncher.exe`, self-updating) |
| `v<version>` | **PROD** builds |
| `unstable-<version>-<commit>` | **UNSTABLE** builds (prereleases, only the last few are kept) |
| `runtime-<hash>` | the shared game engine binary used by builds (downloaded automatically) |

To take over this repository (AI or developer): [HANDOVER.md](HANDOVER.md).

A subsidiary of [Alpharium](https://alpharid.github.io/ACH/#filiale/oddyseus) — α Games division.
