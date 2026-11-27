# Dreamsurf — Development history

## v0.29.5.2 — Three Ways to Ride (release candidate)

Consolidated changes since v0.28.2.7. Final Windows exports and runtime validation are pending.

### What's changed

#### Freestyle
- Higher optional speeds, larger jumps and a new XL big-air feature with longer airtime for full grab spins.
- Symmetrical halfpipe sections with contained wall aerials. The board follows the invisible extension of the lip through ascent and descent while aerial tricks remain available.
- Precision grind rails and wide boxes, now paired for same-rail hops and rail-to-rail transfers.
- 50-50s, boardslides, nosepresses and tailpresses, with dedicated balancing poses, smoother transitions and linked aerial exits.
- New loaded body 360s, directional grab tweaks, alley-oop-style rotations and edge-to-end / end-to-edge butter exchanges.
- A seven-tab trick guide, including a dedicated Park section. The center riding lane remains open for uninterrupted flatland combos.

#### Flow
- Wider carving ribbons, broad banked turns and gentle rollers.
- Final comfort tuning softens the new terrain and allows wider player-chosen carving lines without increasing speed limits.

#### Exploration
- Wider scenic terraces and alternating high/low routes through branching passages.
- New ruins, gardens, overlooks and route-specific discoveries in the exploration journal.
- Still unscored, with no timers or mandatory progression.

#### Teddy and interface
- Shorter, fuller plush limbs, continuous rounded paw geometry and improved hip attachment and board clearance.
- Corrected regular stance, smoother carving arm movement and edge transitions, revised speed-tuck and grind poses.
- Expanded randomized title-screen trick demonstrations using the shared rider rig.
- Unified, more legible settings dialog with explicit Save and discard behavior. Scrolling no longer changes slider values. Version information comes from the project configuration.
- Practice retains its familiar snowy Bunny Slope.

#### Under the hood
- Major source restructuring separates riding, tricks, rigging, terrain, presentation, camera, input, audio and settings into dedicated scripts.
- Expanded regression tests, dependency maps and profiling documentation.
- Previous Freestyle records are preserved; the expanded park uses separate score and combo record categories.
- Windows ANGLE compatibility configuration and Godot licensing notices are retained in the project.


### Final Flow tuning (v0.29.5.1–v0.29.5.2)
- Reduced the additional curve, roller and banking intensity to 17.5% of the original v0.29.5 expansion, while retaining the wider track.
- Independently widened the chosen-line allowance and delayed outward steering attenuation. Existing speed limits and edge rescue remain unchanged.

### Validation and release status
The source archive passed ZIP integrity checks. Independent mathematical tests and 25 engine smoke tests are included; those engine tests have not been run by the build assistant. Final high-speed Flow playtesting, Windows export checks and distribution validation remain pending. See the [prepared release notes](docs/release-v0.29.5.2.md).

---

## v0.28.2.7 — Freestyle Flow

The second public milestone, following [v0.25.12](https://github.com/T3L3SIS/Dreamsurf/releases/tag/v0.25.12). This consolidates the intervening development builds into one release.

### Gameplay
- Expanded flatland tricks: loaded presses, timed snap pops and transfers, extended rotations, rewind pretzels and pivot exchanges.
- Ground-to-air chains, landing catches and reverts; carve and slide setups; late shuvits, aerial continuations and shifties.
- Middle-board grabs, including standalone grabs and a manually controlled whole-rider spin. Hold S in the air, then hold a horizontal trick arrow; release within 25 degrees of regular or switch stance for alignment. Sideways landings can crash.
- Freestyle is now a wider, gentler course with a continuous flat combo lane, optional small/medium/large jumps, advance warnings and side banks. Higher speed is optional; automatic centering is substantially reduced.
- A separate unscored snowy Practice slope, 220 m long, with subdued winter lighting.
- Reorganized six-tab trick guide with execution timing and combo examples. No mandatory tutorials or progression.
- Menu scaling fixes and randomized butter demonstrations on the title screen using the gameplay teddy rig.

### Technical changes
- Customizable movement bindings and dynamic control prompts.
- Terrain streaming priorities, performance diagnostics, safer settings writes and backups, and FLAC decoding safeguards.
- Existing personal records retained; revised freestyle scoring uses separate record keys.
- Windows ANGLE / Direct3D 11 preference addresses an observed Intel Iris Xe native OpenGL x64 startup crash. The developer reports successful launches after the fix.
- Updated Windows export presets and version metadata, plus Godot license and copyright notices.

### Downloads
The planned release assets are Windows x64 (Intel/AMD 64-bit), Windows x32 (32-bit), and the Godot project ZIP. ARM64 is not supplied for this version. The Windows builds are portable: extract the whole archive and launch the EXE. The supplied binaries embed their game resource packs, and do not require Godot to play. For source, extract and import Dreamsurf/project.godot in Godot 4.7.1.

### Compatibility and security
The Windows binaries are unsigned; SmartScreen may warn about an unknown publisher. Keep antivirus enabled, scan the downloaded files and report any detections before running them. Suspected false positives can be submitted to [Microsoft](https://www.microsoft.com/en-us/wdsi/filesubmission). See [checksums](https://github.com/T3L3SIS/Dreamsurf/blob/main/SHA256SUMS.txt) and [Windows notes](https://github.com/T3L3SIS/Dreamsurf/blob/main/WINDOWS.md). Archive integrity and architecture were checked; independent malware scanning and broad hardware testing have not been performed.

Controller support remains deferred. Next development focus: technical maturity and optimization.
