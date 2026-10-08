# Yabause on PS3 — Compatibility & Stability Research

**Date:** 2026-10-08

## Headline Finding

**There is no Yabause libretro core for PS3 in any official libretro/RetroArch PS3 release.** Four independent sources confirm:
1. Final PS3 nightly core archives (CEX Mar 2021, DEX Aug 2020) contain no Yabause/Saturn core among 52 cores
2. libretro's PS3 build script only builds 2048, gambatte, numero, snes9x2010, vecx
3. ConsoleMods PS3:RetroArch wiki core list has no Saturn core
4. libretro docs never mention a PS3 Saturn core

## What Exists

- **libretro Yabause core:** Still maintained (last commit May 30, 2026, 3,356 commits) — but only for mainstream platforms, NOT PS3. Version 0.9.15.
- **Upstream Yabause:** Dead. Last release 0.9.15 (Aug 24, 2016).
- **Only Yabause for PS3 hardware:** Standalone 0.1 beta (2010, Team GEN) — laggy proof-of-concept from 3.55 jailbreak era, not a libretro core.

## CFW Compatibility

RetroArch PS3 runs on **any CFW** (Rebug, Ferrox, Evilnat, etc.) with separate CEX/DEX PKGs. No minimum firmware published. No Yabause-specific CFW issues found (no core exists to have issues).

**Rebug 4.84:** No Yabause-specific issues reported (no core exists). Generic RetroArch PS3 notes: occasional black screen on launch (restart fixes), 1.8.0 aspect-ratio bug — neither CFW-specific.

## Recent Activity (2023-2026)

Nothing PS3-specific. Found:
- Kodi addon 3D-pad fix (2026-08-18)
- Launchpad nightly builds (2026-08-23)
- WebOS rebuild: yabause among failed builds (Dec 2025)
- libretro/yabause: 8 open issues, none PS3-related

## Sources

- https://docs.libretro.com/library/yabause/
- https://github.com/libretro/yabause (verified live 2026-10-08)
- https://emulation.gametechwiki.com/index.php/Sega_Saturn
- https://emulation.gametechwiki.com/index.php/Yabause
- https://consolemods.org/wiki/PS3:RetroArch
- https://docs.libretro.com/guides/install-ps3/
- https://github.com/libretro/libretro-super/blob/master/libretro-build-sncps3.sh
