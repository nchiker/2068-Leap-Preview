# 2068 Leap — Public Preview

2068 Leap is an alternate-history ROM for the Timex Sinclair 2068: a
structured, line-number-free BASIC with a full-screen editor, Timex
high-resolution graphics, sprites, AY sound, ULAplus palettes, arrays,
strings, and stock-framed `SAVE`/`LOAD` support.

This repository distributes ready-to-run preview builds and documentation.
Development source remains in a separate private repository during preview
testing.

## Files in this repository

Everything needed to try the preview is also visible in the repository:

- [`roms/`](roms/) — Home ROM, EXROM, combined ZEsarUX image, and checksums;
- [`docs/`](docs/) — Word user manual and all Markdown reference documents;
- [`demos/`](demos/) — showcase and smoke-test BASIC programs.

The same files, plus a single documentation ZIP, are attached to the
[Public Preview 1 release](../../releases/tag/v0.1.0-preview.1) for convenient
one-page downloading.

## Run in Fuse

```sh
fuse --machine ts2068 \
  --rom-ts2068-0 test_basic.bin \
  --rom-ts2068-1 exrom.bin
```

The EXROM image belongs in slot 6. Upstream Fuse may not expose ULAplus on
the TS2068, but the rest of the ROM remains testable.

## Run in ZEsarUX

```sh
zesarux --noconfigfile --machine TS2068 \
  --romfile ts2068rom_zesarux.bin --enableulaplus
```

## Preview status

The preview passed 68 integrated BASIC fixtures, standalone ROM smoke tests,
an automated wrapped-line editor test, and showcase validation. It remains
pre-1.0 software; keep backups of saved programs because its native program
payload may still evolve.

Please use this repository's Issues page for reproducible preview feedback.
Include the emulator and version, host operating system, commands entered,
and the smallest program that demonstrates the problem.

2068 Leap is released under the MIT License.
