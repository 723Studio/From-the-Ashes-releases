# X-Com: From the Ashes Releases

Public download hub for **X-Com: From the Ashes**.

From the Ashes is a standalone X-COM-inspired game built on a fork of the OpenXcom / OpenXcom Extended engine lineage. This repository contains public release artifacts: Windows and Linux builds, checksums, release manifests, and GPL engine source archives.

## Download

| Channel | Status | Link |
| --- | --- | --- |
| Stable | Not published yet | Placeholder: stable 1.6.0 will appear here after RC validation |
| Pre-release | Current public playtest build | [From the Ashes 1.6.0 RC1](https://github.com/723Studio/From-the-Ashes-releases/releases/tag/v1.6.0-rc.1) |
| Nightly | Not published yet | Placeholder: nightly builds will appear here after release automation is finished |

Most testers should start with the Windows x64 package from the latest pre-release:

```text
FTA-<version>-<channel>-windows-x64.zip
```

Linux testers can use the AppImage package:

```text
FTA-<version>-<channel>-x86_64.AppImage
```

## Current testing focus

The current public build is a release candidate, not a stable release.

The most useful test right now is a full playthrough of the available Alpha 2 campaign up to and including the current finale: **the assault on the MIB HQ**.

Full playthrough videos uploaded to YouTube or another video host are especially valuable, because they show pacing, balance, confusion points, UI friction, and bugs that are easy to miss in short reports.

## What to report

Please report crashes, bugs, balance problems, missing resources, progression blockers, package loading issues, and unexpected modified/untrusted mode behavior.

For crashes, please include a save file shortly before the crash, the game log, what you did immediately before the crash, and whether the crash is reproducible from the save.

For balance and progression issues, please include as much context as possible: campaign date, squad state, equipment, research, mission type, enemy type, and what felt wrong.

Feedback channels:

- OpenXcom forum board: https://openxcom.org/forum/index.php?board=27.0
- Discord: https://discord.gg/8sgFYhrw6t

## Source code

The GPL engine source corresponding to release binaries is provided in two forms:

- source archive attached to each binary release, for example `fta-engine-source-<version>.tar.gz`;
- public generated engine source mirror: https://github.com/723Studio/From-the-Ashes-engine

The engine source mirror is generated from the private development monorepo's `engine/` subtree and tagged for public releases. Official From the Ashes game content is distributed separately from the GPL engine source mirror.

## Engine lineage and acknowledgements

From the Ashes exists because of the work of the OpenXcom and OpenXcom Extended communities.

Special thanks and respect to:

- **OpenXcom** — https://github.com/OpenXcom/OpenXcom
- **OpenXcom Extended / OXCE** — https://github.com/MeridianOXC/OpenXcom

FTA uses a forked engine derived from this lineage. The public engine source mirror for FTA releases is maintained separately from game content.

## Credits and third-party materials

From the Ashes uses and adapts materials created by members of the OpenXcom modding community, with author permission and/or under compatible community licensing terms.

Credits for contributors and community material sources are maintained in:

[Credits and third-party materials](CREDITS.md)

## Release files

A complete public release normally contains:

- Windows x64 zip build;
- Linux AppImage;
- Linux fallback tar.gz package;
- GPL engine source archive;
- `manifest.json`;
- `sha256sums.txt`;
- Linux runtime dependency report.

Use `sha256sums.txt` to verify downloads.

## For new players

From the Ashes is still in active alpha development. Expect rough edges, balance changes, missing polish, and occasional save-breaking updates between pre-release builds.

If you want the smoothest experience, wait for a stable release. If you want to help shape the project, play the latest pre-release and send detailed feedback.
