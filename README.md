# 2068-Leap — Release 1 Beta

2068-Leap is an alternate-history ROM for the Timex Sinclair 2068: a
structured, line-number-free BASIC with a full-screen editor, Timex
high-resolution graphics, sprites, AY sound, ULAplus palettes, arrays,
strings, and stock-framed `SAVE`/`LOAD` support.

This repository distributes the ready-to-run Release 1 Beta images,
loadable extensions, and documentation.

## Files in this repository

Everything needed to try the preview is also visible in the repository:

- [`roms/`](roms/) — Home ROM, raw EXROM, EightyOne cartridge, and combined
  ZEsarUX image;
- [`extensions/`](extensions/) — CPLOT, BLOCK, FRAME, INVERT, AYREG, and OUT
  tape images;
- [`docs/`](docs/) — Word user manual and all Markdown reference documents;
- [`docs/whats_new_release_1_beta.md`](docs/whats_new_release_1_beta.md) — a
  preview-to-beta guide, also supplied as a styled Word document;
- [`demos/`](demos/) — showcase and smoke-test BASIC programs.
- [`SHA256SUMS.txt`](SHA256SUMS.txt) — checksums for every distributed binary
  and tape image.

See the [complete emulator setup guide](docs/emulator_setup.md) before choosing
files. The GitHub beta release should attach the same files for convenient
one-page downloading.

## Run in Fuse

```sh
fuse --machine ts2068 \
  --rom-ts2068-0 roms/test_basic.bin \
  --rom-ts2068-1 roms/exrom.bin
```

The EXROM image belongs in slot 6. Upstream Fuse may not expose ULAplus on
the TS2068, but the rest of the ROM remains testable.

## Run in ZEsarUX

```sh
zesarux --noconfigfile --machine TS2068 \
  --romfile roms/ts2068rom_zesarux.bin --enableulaplus
```

## Run in EightyOne 1.41

Select the TS2068 machine, use `roms/test_basic.bin` as the ROM file, and use
`roms/exrom.dck` as a **Timex ROM Cartridge**. Do not select raw `exrom.bin` in
the cartridge field. Detailed dialog-by-dialog instructions are in the
[emulator setup guide](docs/emulator_setup.md#eightyone-141).

## Load optional BASIC commands

Open the required file from [`extensions/`](extensions/) in the emulator's
tape controls, then enter `LOAD "name" EXT`. Only one module is installed at a
time; load an ordinary BASIC program before loading its required extension.

## Beta status

The beta passes all 92 integrated BASIC fixtures, the static/build gate, and
15 standalone ROM builds. It remains beta software; keep backups of saved
programs because its native program payload may still evolve before the final
Release 1 build.

Please use this repository's Issues page for reproducible beta feedback.
Include the emulator and version, host operating system, commands entered,
and the smallest program that demonstrates the problem.

2068-Leap is released under the MIT License.
