# HANDOVER - oddyseus-fst-builds

> Last updated: 2026-09-30. Owner: Alpharid (French speaker; docs in English).

## What this repository is
The **public distribution channel** of the private game repo `Alpharid/oddyseus-fst` (Godot 4.7.2 coop FPS "Oddyseus : F.S.T."). It contains **no source and no binaries in git**: only this documentation. All artifacts live in **GitHub Releases** and are produced by `tools/publish.py` of the private repo. Nothing here is edited by hand.

## Contract with the launcher (private repo `launcher/`)
The launcher reads `GET https://api.github.com/repos/Alpharid/oddyseus-fst-builds/releases` (anonymous) and picks:
* PROD = newest non-prerelease whose tag starts with `v`; asset `manifest.json` + `game.pck.zip`
* UNSTABLE = newest release whose tag starts with `unstable-`
* launcher update = release tagged `launcher` (`launcher-manifest.json`, `OddyseusLauncher.zip`, plus the bare `OddyseusLauncher.exe` for first download)
* `runtime-<sha8>` releases hold `runtime.zip` (the engine exe shared by builds); a build manifest names the release it needs (`files[].release`).

`manifest.json` schema 1: `channel, version, commit, built_at, build_id ("<version>|<channel>|<commit>"), engine, min_launcher, files[{name, asset, release?, shared?, size, zip_size, sha256, zip_sha256}]`. The launcher verifies every sha256 and writes its own `manifest.json` into the build folder last.

## Rules
* Never delete a `runtime-*` release that a still-listed build manifest references; only `unstable-*` releases are pruned (last 3 kept).
* Never rename tags or asset names: the launcher relies on them.
* Repo stays public (the launcher downloads anonymously); do not put secrets or source here.

## Publishing (from the private repo)
`python tools/publish.py prod|unstable|launcher` (see HANDOVER.md section 3b there).
