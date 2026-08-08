# X-Com: From the Ashes Releases

Public download hub for **X-Com: From the Ashes**.

From the Ashes is a self-contained game built from the OpenXcom / OpenXcom Extended engine lineage. This repository contains public Windows and Linux builds, checksums, release manifests, and GPL-covered executable source archives.

## Current recommended build

**Version:** `v0.2.0`  
**Milestone:** Alpha 2  
**GitHub status:** Pre-release  
**Download:** [X-Com: From the Ashes 0.2.0 — Alpha 2](https://github.com/723Studio/From-the-Ashes-releases/releases/tag/v0.2.0)

Alpha 2 is an active-development build intended for broad gameplay testing. It contains the current early-game and midgame campaign slice and still needs balance, progression, UX, and stability feedback.

## Important: clean installation required

**Save games and options from the legacy `1.6.0` builds are not compatible with `0.2.0`. Do not continue an old campaign and do not reuse the old `options.cfg`.**

Before starting `0.2.0` on Windows:

1. Back up screenshots or logs that you want to keep.
2. Delete the complete folder:

   ```text
   %USERPROFILE%\Documents\OpenXcomFtA
   ```

3. Recreate the folder and copy your legally owned original X-COM / UFO Defense resources into:

   ```text
   %USERPROFILE%\Documents\OpenXcomFtA\UFO
   ```

4. Extract the new FTA release into a normal game folder.
5. Start a completely new campaign.

A correct original-resource folder contains directories such as:

```text
%USERPROFILE%\Documents\OpenXcomFtA\UFO\GEODATA
%USERPROFILE%\Documents\OpenXcomFtA\UFO\GEOGRAPH
%USERPROFILE%\Documents\OpenXcomFtA\UFO\MAPS
%USERPROFILE%\Documents\OpenXcomFtA\UFO\ROUTES
%USERPROFILE%\Documents\OpenXcomFtA\UFO\TERRAIN
%USERPROFILE%\Documents\OpenXcomFtA\UFO\UNITS
```

Linux testers should remove or rename their previous FTA data and configuration directories before starting a new campaign:

```text
~/.local/share/openxcomfta
~/.config/openxcomfta
```

When `XDG_DATA_HOME` or `XDG_CONFIG_HOME` is configured, use the corresponding `openxcomfta` directories instead. Restore the original game files as a clean `UFO` folder in the FTA data directory.

## Major changes in 0.2.0

- fixed a large number of engine, content, progression, UI, and ruleset defects;
- substantially reworked the **Intelligence system**;
- refined the **main story chain** and its progression flow;
- completely redesigned the systems for **capturing, containing, and studying monsters and aliens**;
- introduced one unified FTA project version across the executable, saves, public tags, manifests, and binary artifacts.

## Current testing focus

The most valuable test is a complete fresh playthrough of all currently available Alpha 2 content.

The main question is:

> **Can you reach and successfully destroy the MIB Regional HQ?**

Please report where progression stopped even when you did not reach the HQ. Reports about missing missions, research or Intelligence dead ends, unclear objectives, balance spikes, crashes, broken maps, capture/containment problems, and unexpected modified/untrusted status are especially useful.

Full-playthrough recordings are also valuable because they expose pacing, balance, UI friction, unclear rules, and narrative sequencing problems that are difficult to reconstruct from short reports.

## Download files

A complete `0.2.0` release contains:

```text
FTA-0.2.0-windows-x64.zip
FTA-0.2.0-x86_64.AppImage
fta-linux-0.2.0.tar.gz
fta-engine-source-0.2.0.tar.gz
linux-runtime-deps.txt
manifest.json
sha256sums.txt
```

For most players:

- Windows: download `FTA-0.2.0-windows-x64.zip`;
- Linux: try `FTA-0.2.0-x86_64.AppImage` first;
- advanced Linux users can use `fta-linux-0.2.0.tar.gz`.

All public releases are available at:

https://github.com/723Studio/From-the-Ashes-releases/releases

## GitHub release status

FTA uses one version-only tag for each published project version, for example:

```text
v0.2.0
v0.2.1
v1.0.0
```

GitHub displays one of two release statuses:

- **Pre-release** for active-development Alpha and Beta builds;
- **Latest** for the currently recommended completed release.

The status does not change the version tag or artifact names. A published version is not replaced or retagged; the next publication uses a new project version.

## Required original game files

FTA does not include files from X-COM: UFO Defense / UFO: Enemy Unknown.

You need resources from a legally owned copy of the original game. These files cannot be redistributed with FTA. If the game reports:

```text
required external resource folders are missing: UFO
```

then the original resources are missing, incomplete, or stored in the wrong location.

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
Get-FileHash ".\FTA-0.2.0-windows-x64.zip" -Algorithm SHA256
```

Compare the calculated value with the corresponding line in `sha256sums.txt`.

## Bug reports

Please include:

- FTA version and build ID from `openxcom.log`;
- operating system and package type;
- exact reproduction steps;
- exact error or crash message;
- `openxcom.log`;
- a save shortly before the issue, when possible;
- a screenshot for visible UI, map, or localization problems;
- campaign date, research state, equipment, and mission context for progression or balance issues.

Feedback channels:

- OpenXcom forum: https://openxcom.org/forum/index.php?board=27.0
- Discord: https://discord.gg/8sgFYhrw6t

## GPL executable source

The matching GPL-covered executable source is available in two forms:

- `fta-engine-source-0.2.0.tar.gz` attached to the release;
- the public source mirror tagged `v0.2.0`:
  https://github.com/723Studio/From-the-Ashes-engine

The source mirror contains no proprietary FTA content, encrypted official packages, private assets, original UFO data, or release secrets.

## Engine lineage and acknowledgements

From the Ashes exists because of the work of the OpenXcom and OpenXcom Extended communities.

- **OpenXcom:** https://github.com/OpenXcom/OpenXcom
- **OpenXcom Extended / OXCE:** https://github.com/MeridianOXC/OpenXcom

Credits for contributors and third-party community materials are maintained in [CREDITS.md](CREDITS.md).
