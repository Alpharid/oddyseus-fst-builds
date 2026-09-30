# Oddyseus : F.S.T. - builds

Public release channel of **Oddyseus : F.S.T.**, a 1-8 player coop first-person immersive sim (Godot 4.7).
This repository only carries **binaries** (as GitHub Releases); the source code is private.

## Play

1. Download **[`OddyseusLauncher.exe`](https://github.com/Alpharid/oddyseus-fst-builds/releases/tag/launcher)** once and keep it (Windows 10/11 64-bit, Vulkan GPU).
   Windows SmartScreen may warn because the exe is not code-signed: *More info* > *Run anyway*.
2. Start it, pick **PROD** (stable) or **UNSTABLE** (newest features, may break), press *Install & play*.
   The launcher downloads and verifies the build, updates itself and the game, and never needs to be re-sent.
3. In the game: *Host* (you can start alone) or *Join* (paste the host's link). Everybody in a game must run the **same build** (same channel and version) - the game refuses the connection otherwise.

## Releases

| tag | what |
|---|---|
| `launcher` | the launcher (`OddyseusLauncher.exe`, self-updating) |
| `v<version>` | **PROD** builds |
| `unstable-<version>-<commit>` | **UNSTABLE** builds (prereleases, the last few are kept) |
| `runtime-<hash>` | the shared game engine binary used by builds (downloaded automatically) |

See [HANDOVER.md](HANDOVER.md) for how this repository is produced and consumed.
