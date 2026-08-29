# Preview testing guide

Useful areas for public-preview testing include:

- editor navigation, word wrapping, insertion, deletion, and error display;
- `SAVE`/`LOAD`, including named and empty-name loads;
- numeric and string arrays;
- normal and Timex high-resolution graphics;
- sprites and collision detection;
- AY sound;
- ULAplus palette entry and return to the normal editor display;
- longer programs that combine several subsystems.

When reporting an issue, include:

1. Emulator and exact version, or real TS2068 hardware details.
2. Which ROM files were installed and where.
3. The shortest BASIC program or keystroke sequence that reproduces it.
4. Expected and observed behavior.
5. A screenshot, saved program, or memory dump when available.

Do not include private information in public issues.

For EightyOne, leave randomized power-on RAM enabled when possible. The
corrected preview initializes its owned RAM and should boot consistently
without relying on the emulator to clear memory. See
[`docs/eightyone_setup.md`](docs/eightyone_setup.md) for version 1.41 setup.
