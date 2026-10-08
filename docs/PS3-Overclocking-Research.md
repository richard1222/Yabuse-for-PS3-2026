# PS3 Overclocking for Saturn (Yabause) Emulation — Research

**Date:** 2026-10-08  
**Hardware:** PS3 Slim 2001A (62nm Cell)

## Headline Finding

**No one overclocks a PS3 for Saturn emulation — and there's a structural reason why it wouldn't help.**

Every mainstream PS3 overclock method (Evilnat CFW + Cobra `overclock.txt`) overclocks **only the RSX GPU**:
- Stock: 500 MHz core / 650 MHz memory
- Typical OC: 600 MHz core / 750 MHz memory
- **Cell CPU stays at 3.2 GHz** — untouched

Yabause on PS3 is **CPU-bound** (interpreter-only; the fast dynarec can't be used in libretro cores). Overclocking the RSX will not measurably improve Saturn emulation speed.

## Saturn on PS3: The Reality

Saturn is by far the worst-supported system on PS3 homebrew:
- **No Saturn core** in RetroArch PS3's stable set
- **No PS1 core, no N64 core** either
- Only option: standalone Yabause 0.1 alpha (2010) — described at launch as "don't expect miracles in speed or compatibility"
- Saturn emulation is CPU-intensive even on modern hardware

**Bottom line:** Saturn on PS3 is effectively non-viable regardless of overclocking.

## Overclock Speeds (for reference)

| Setting | RSX Core | RSX Memory | Notes |
|---------|----------|------------|-------|
| Stock | 500 MHz | 650 MHz | Factory |
| Community standard | 600 MHz | 750 MHz | Most tested; +7-19% FPS in GPU-bound games |
| Evilnat max | 1050 MHz | — | Hard cap, NOT a recommendation |

**Method (Evilnat CFW):** Create `overclock.txt` (line 1 = core MHz, line 2 = memory MHz), place at `/dev_usb000/overclock.txt` or `/dev_hdd0/overclock.txt`, restart. Verify via XMB Network > Custom Firmware Tools > Overclock Tools.

## Slim 2001A Specifics

- All CECH-2000 series can run CFW → software OC method works
- 62nm Cell runs cooler than Fat models (90nm/65nm) → better thermal headroom
- No community "safe" table exists for 2000 series specifically
- 600/750 is the de-facto starting point; stability varies per console

## Risks

- **No verified reports** of PS3s dying specifically from RSX overclocking
- Risk is thermal: ~95% of YLOD cases attributed to heat-cracked RSX solder balls (iFixit)
- YLOD guides explicitly warn: "Avoid Overclocking"
- Mitigations: higher fan speeds, repaste, monitor temps via webMAN MOD, stay near 600/750

## Which Emulators Benefit?

- **GPU-bound:** Commercial PS3 games (main use case for OC)
- **CPU-bound (no benefit from RSX OC):** MAME, SuperFX/SA-1 SNES, PUAE, PrBoom, **Yabause/Saturn**
- Cell CPU overclocking is experimental 2025 research (syscon patching) — not an end-user tool yet

## Sources

- PSX-Place Evilnat 4.92.2/4.93 threads (OC how-to)
- NeoGAF "Stock vs Overclocked PS3" (600/750 FPS data)
- Emulation General Wiki: Emulators on PlayStation 3 (verified live)
- Exophase: Yabause PS3 port (2010)
- iFixit: YLOD causes
- libretro forums: dynarec discussion (hunterk)
