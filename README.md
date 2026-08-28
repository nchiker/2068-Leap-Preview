# 2068 Leap — Public Preview

2068 Leap is an alternate-history ROM for the Timex Sinclair 2068: a
structured, line-number-free BASIC with a full-screen editor, Timex
high-resolution graphics, sprites, AY sound, ULAplus palettes, arrays,
strings, and stock-framed `SAVE`/`LOAD` support.

This repository distributes ready-to-run preview builds and documentation.
Development source remains in a separate private repository during preview
testing.

## Download

Open the [latest release](../../releases/latest) and download:

- `test_basic.bin` and `exrom.bin` for a TS2068 emulator with separate Home
  ROM and EXROM images;
- `ts2068rom_zesarux.bin` for ZEsarUX;
- `2068_Leap_Users_Manual.docx` or the complete documentation ZIP;
- `RELEASE_SHA256SUMS.txt` to verify the ROM downloads.

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
