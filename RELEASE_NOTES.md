# 2068 Leap Public Preview 1

This is the first public, test-gated preview of 2068 Leap for Timex Sinclair
2068 users and emulator testers.

## Highlights

- Structured, line-number-free BASIC with a full-screen editor.
- Numeric scalars and arrays, fixed-length strings and string arrays.
- Timex high-resolution graphics, Spectrum graphics, sprites, AY sound, and
  ULAplus palette control with editor-safe mode restoration.
- Stock TS2068/Sinclair tape framing for `SAVE` and `LOAD`, including progress
  reporting and validation before replacing the current program.
- Screen queries through `POINT()` and `ATTR()`.
- Styled Word user manual and a complete documentation bundle.

## Validation baseline

- 68 integrated BASIC fixtures pass.
- Nine standalone smoke ROMs assemble successfully.
- Automated wrapped-line editor regression passes.
- Showcase validation reaches its green completion border.
- Home ROM has 13 bytes free; EXROM has 99 bytes free; the dynamic RAM pool is
  1857 bytes.

## Corrected preview build

- Cold start now initializes the complete ROM-owned `$8000-$BFFF` RAM region.
  This fixes inconsistent startup in emulators that randomize RAM on a hard
  reset.
- `roms/exrom.dck` packages the EXROM for the Timex ROM Cartridge field in
  EightyOne v1.41. See `docs/eightyone_setup.md`.

## Important preview boundary

2068 Leap is a redesigned BASIC, not a byte-compatible replacement for stock
Sinclair BASIC programs. Saved programs use standard TS2068 tape framing but
carry 2068 Leap's native, non-tokenized program payload. Keep backups of work
created with preview builds.
