# Release 1 Beta asset checklist

Publish these files with the GitHub beta release. They are generated together
from the validated source build; do not mix files from different builds.

## Emulator images

| Asset | Required for |
|---|---|
| `test_basic.bin` | Fuse Home ROM; EightyOne ROM File |
| `exrom.bin` | Fuse TS2068 EXROM |
| `exrom.dck` | EightyOne 1.41 Timex ROM Cartridge |
| `ts2068rom_zesarux.bin` | ZEsarUX combined ROM |

## Loadable extensions

Attach `cplot.tzx`, `block.tzx`, `frame.tzx`, `invert.tzx`, `ayreg.tzx`, and
`out.tzx`. These are the emulator/cassette-ready forms of the optional BASIC
modules; internal assembler test binaries are not release assets.

## Documentation

- `2068_Leap_Users_Manual.docx`
- `user_manual.md`
- `2068-Leap_Whats_New_Release_1_Beta.docx`
- `whats_new_release_1_beta.md`
- `emulator_setup.md`
- `RELEASE_NOTES.md`
- `ANNOUNCEMENT_RELEASE_1_BETA.md`
- `SHA256SUMS.txt`
- `LICENSE`
- `0001-Add-ULAplus-support-for-Timex-machines.patch` (optional Fuse ULAplus support)

## Pre-publication checks

1. Verify all hashes from the repository root with `sha256sum -c SHA256SUMS.txt`.
2. Confirm `test_basic.bin` is 16,384 bytes, `exrom.bin` is 8,192 bytes,
   `exrom.dck` is 8,201 bytes, and the combined image is 24,576 bytes.
3. Confirm the combined image equals `test_basic.bin` followed by `exrom.bin`.
4. Confirm the DCK payload after its nine-byte header equals `exrom.bin`.
5. Keep the release marked **pre-release** on GitHub until physical-hardware and
   cassette feedback meets the final Release 1 gate.
