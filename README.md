# X-Com: From the Ashes Releases

Public download hub for **X-Com: From the Ashes**.

From the Ashes is a self-contained game built from the OpenXcom / OpenXcom Extended engine lineage. This repository contains public Windows and Linux builds, checksums, release manifests, and GPL-covered executable source archives.

## Current recommended build

| Channel | Status | Link |
| --- | --- | --- |
| Stable | Not published yet | Alpha 2 is still being validated through release candidates |
| Release Candidate | **Current recommended public playtest** | [X-Com: From the Ashes 0.2.0 — Alpha 2 RC1](https://github.com/723Studio/From-the-Ashes-releases/releases/tag/v0.2.0-rc.1) |
| Nightly | Not published currently | Nightly builds are experimental development snapshots |

Version `0.2.0-rc.1` is intended for broad gameplay testing. It is not the finished game: Alpha 2 covers the current early-game and midgame slice and still needs balance, progression, UX, and stability feedback.

## Important: clean installation required

**Save games and options from the previous `1.6.0` builds are not compatible with `0.2.0`. Do not continue an old campaign and do not reuse the old `options.cfg`.**

For Windows, the recommended upgrade procedure is:

1. Exit FTA.
2. Back up screenshots or logs that you want to keep.
3. Delete the complete folder:

```text
%USERPROFILE%\Documents\OpenXcomFtA
```

4. Start from a clean `OpenXcomFtA` folder.
5. Copy the files from a legally owned installation of the original X-COM: UFO Defense / UFO: Enemy Unknown into:

```text
%USERPROFILE%\Documents\OpenXcomFtA\UFO
```

A valid resource path should contain folders such as:

```text
%USERPROFILE%\Documents\OpenXcomFtA\UFO\GEODATA
%USERPROFILE%\Documents\OpenXcomFtA\UFO\GEOGRAPH
%USERPROFILE%\Documents\OpenXcomFtA\UFO\MAPS
%USERPROFILE%\Documents\OpenXcomFtA\UFO\ROUTES
%USERPROFILE%\Documents\OpenXcomFtA\UFO\TERRAIN
%USERPROFILE%\Documents\OpenXcomFtA\UFO\UNITS
```

For Linux, remove or rename the previous FTA user-data and configuration directories before testing the new release. The default paths are:

```text
~/.local/share/openxcomfta
~/.config/openxcomfta
```

If `XDG_DATA_HOME` or `XDG_CONFIG_HOME` is configured, use the corresponding `openxcomfta` directory there. Put the original game resources in the clean data directory as `UFO`.

## Alpha 2 RC1 highlights

This release contains a large accumulated maintenance and systems pass:

- fixes for a large number of engine, content, progression, UI, and ruleset defects;
- a substantially reworked **Intelligence** system;
- a refined main story chain and progression flow;
- a complete redesign of capturing, containing, and studying monsters and aliens;
- unified FTA project versioning across the executable, saves, release tags, manifests, and artifacts.

## Current testing focus

The most valuable test is a full fresh campaign through all currently available Alpha 2 content.

The main question is:

> **Can you reach and successfully destroy the MIB Regional HQ?**

Please report progression blockers, unclear objectives, missions that never appear, research loops, balance spikes, missing resources, crashes, and any state where the campaign can no longer advance.

Full-playthrough recordings are especially useful because they expose pacing, balance, UI friction, unclear rules, and narrative sequencing problems that are difficult to reproduce from a short bug report.

## Download files

The RC1 release contains:

```text
FTA-0.2.0-rc.1-windows-x64.zip
FTA-0.2.0-rc.1-x86_64.AppImage
fta-linux-0.2.0-rc.1.tar.gz
fta-engine-source-0.2.0.tar.gz
manifest.json
sha256sums.txt
linux-runtime-deps.txt
```

For most players:

- Windows users should download `FTA-0.2.0-rc.1-windows-x64.zip`;
- Linux users should try `FTA-0.2.0-rc.1-x86_64.AppImage` first;
- advanced Linux users can use `fta-linux-0.2.0-rc.1.tar.gz`.

All public releases are available at:

https://github.com/723Studio/From-the-Ashes-releases/releases

## Required original game resources

FTA does not include files from the original X-COM: UFO Defense / UFO: Enemy Unknown.

You must provide the resources from a legally owned copy of the original game. Do not report startup errors until the clean `UFO` folder has been restored in the expected data location.

## Checksums and verification

Each complete release contains:

```text
sha256sums.txt
manifest.json
```

On Linux:

```bash
sha256sum -c sha256sums.txt
```

On Windows PowerShell:

```powershell
Get-FileHash ".\FTA-0.2.0-rc.1-windows-x64.zip" -Algorithm SHA256
```

Compare the calculated value with `sha256sums.txt` from the same release.

## Bug reports

Please include:

- FTA version and build ID;
- operating system;
- package type: Windows zip, Linux AppImage, or Linux tar.gz;
- exact reproduction steps;
- the relevant save file when possible;
- `openxcom.log` and crash information;
- screenshots for visible UI, map, or localization defects;
- campaign date, research state, equipment, and mission context for balance or progression reports.

Feedback channels:

- OpenXcom forum: https://openxcom.org/forum/index.php?topic=13136.0
- Discord: https://discord.gg/8sgFYhrw6t

## Release channels

**Stable** means the most thoroughly validated build of the current development milestone. It does not mean that the full game is complete.

**Release Candidate** builds have passed build and startup checks and are published for broader gameplay validation before a stable build is selected.

**Nightly** builds are experimental snapshots containing very recent changes. They may be incomplete, unstable, or save-incompatible and are intended for targeted testing.

## GPL executable source

The GPL-covered executable source corresponding to public binaries is available in two forms:

- `fta-engine-source-0.2.0.tar.gz` attached to the release;
- the tagged public source mirror: https://github.com/723Studio/From-the-Ashes-engine

The source mirror is generated from the private development monorepo's GPL-covered `engine/` subtree. It has no independently maintained product version; its tags correspond to complete FTA releases. Proprietary FTA content, encrypted official packages, private assets, original game resources, and release secrets are not part of the source mirror.

## Credits and upstream lineage

From the Ashes is derived from the work of the OpenXcom and OpenXcom Extended communities:

- OpenXcom: https://github.com/SupSuper/OpenXcom
- OpenXcom Extended / OXCE: https://github.com/MeridianOXC/OpenXcom

Credits for contributors and third-party community materials are maintained in:

[Credits and third-party materials](CREDITS.md)
