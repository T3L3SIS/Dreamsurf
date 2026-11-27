# Dreamsurf v0.28.2.7 — Freestyle Flow

The second public milestone, following [v0.25.12](https://github.com/T3L3SIS/Dreamsurf/releases/tag/v0.25.12). This consolidates the intervening development builds into one release.

## Gameplay
- Expanded flatland tricks: loaded presses, timed snap pops and transfers, extended rotations, rewind pretzels and pivot exchanges.
- Ground-to-air chains, landing catches and reverts; carve and slide setups; late shuvits, aerial continuations and shifties.
- Middle-board grabs, including standalone grabs and a manually controlled whole-rider spin. Hold S in the air, then hold a horizontal trick arrow; release within 25 degrees of regular or switch stance for alignment. Sideways landings can crash.
- Freestyle is now a wider, gentler course with a continuous flat combo lane, optional small/medium/large jumps, advance warnings and side banks. Higher speed is optional; automatic centering is substantially reduced.
- A separate unscored snowy Practice slope, 220 m long, with subdued winter lighting.
- Reorganized six-tab trick guide with execution timing and combo examples. No mandatory tutorials or progression.
- Menu scaling fixes and randomized butter demonstrations on the title screen using the gameplay teddy rig.

## Technical changes
- Customizable movement bindings and dynamic control prompts.
- Terrain streaming priorities, performance diagnostics, safer settings writes and backups, and FLAC decoding safeguards.
- Existing personal records retained; revised freestyle scoring uses separate record keys.
- Windows ANGLE / Direct3D 11 preference addresses an observed Intel Iris Xe native OpenGL x64 startup crash. The developer reports successful launches after the fix.
- Updated Windows export presets and version metadata, plus Godot license and copyright notices.

## Downloads
The planned release assets are Windows x64 (Intel/AMD 64-bit), Windows x32 (32-bit), and the Godot project ZIP. ARM64 is not supplied for this version. The Windows builds are portable: extract the whole archive and launch the EXE. The supplied binaries embed their game resource packs, and do not require Godot to play. For source, extract and import Dreamsurf/project.godot in Godot 4.7.1.

## Compatibility and security
The Windows binaries are unsigned; SmartScreen may warn about an unknown publisher. Keep antivirus enabled, scan the downloaded files and report any detections before running them. Suspected false positives can be submitted to [Microsoft](https://www.microsoft.com/en-us/wdsi/filesubmission). See [checksums](https://github.com/T3L3SIS/Dreamsurf/blob/main/SHA256SUMS.txt) and [Windows notes](https://github.com/T3L3SIS/Dreamsurf/blob/main/WINDOWS.md). Archive integrity and architecture were checked; independent malware scanning and broad hardware testing have not been performed.

Controller support remains deferred. Next development focus: technical maturity and optimization.
