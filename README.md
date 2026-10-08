# Yabause for PS3

This page is about **Yabause on the PlayStation 3** — the Sega Saturn emulator port for jailbroken PS3 consoles.

## What is Yabause?

Yabause is a free, open-source emulator for the **Sega Saturn** — Sega's 32-bit game console from the mid-1990s (home of NiGHTS, Panzer Dragoon, Virtua Fighter, and Sega Rally).

The Saturn is famously one of the hardest consoles to emulate. It has two main CPUs plus several helper chips all working at once, so emulating it takes a lot of processing power. Yabause is one of the emulators that tries to do it accurately, and it was ported to run on the PS3.

## What does it do on PS3?

On a jailbroken PS3, the Yabause port lets you:

- **Play Sega Saturn games** from disc images (ISO/BIN/CUE files) on your PS3.
- **Use your PS3 controller** as the Saturn gamepad.
- **Save and load** your progress with save states, even in games that never had saves.

A heads-up on expectations: Saturn emulation is heavy, and this is an old port. Don't expect every game to run full speed — 2D games generally fare better than 3D ones.

## What do you need?

- A **jailbroken PS3** — custom firmware (CFW) or HEN. This does not run on a stock, unmodified PS3.
- The Yabause PS3 `.pkg` file, installed via Package Manager → Install Package Files.
- Your own Sega Saturn game files (disc images). A Saturn BIOS file helps a lot with compatibility — only use copies of games and BIOS you own.

## Setup on PS3

1. Copy the `.pkg` to a FAT32 USB drive, plug it into the PS3, and install it via Package Manager → Install Package Files.
2. Make a folder like `/dev_hdd0/ROMS/SATURN` on the PS3 hard drive for your game images.
3. If you have a Saturn BIOS file, place it where the emulator expects it (check the emulator's settings / docs).
4. Start Yabause from the XMB, point it at your game image, and play.

## Screenshots

![Yabause running the Sega Saturn boot screen](https://files.catbox.moe/ex8uo0.jpg)
*Yabause running the Sega Saturn boot screen*

![Yabause running a Saturn game](https://files.catbox.moe/whc2iq.webp)
*Yabause running a Saturn game*

## Good to know

- This is a community homebrew port from the early PS3 homebrew era — it is not officially supported by the Yabause team.
- If a game runs slowly or glitches, try a different game — compatibility varies a lot per title.
- Only use game files and BIOS from stuff you own.

## Links

- [Yabause official site](http://yabause.org/)
- [PS3 Brewology](https://ps3.brewology.com/)
