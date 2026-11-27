# Windows compatibility and distribution

## Installation
Extract the entire downloaded ZIP. Launch the EXE in the extracted folder. The supplied v0.28.2.7 Windows packages contain embedded game resources and Godot notices. Choose x64 for Intel/AMD 64-bit Windows; x32 is the 32-bit alternative. An ARM64 archive is also listed on the v0.28.2.7 release page; its runtime and contents were not independently verified. Check the assets of the specific version you download.

## Graphics
A native OpenGL crash was observed on Intel Iris Xe with igxelpicd64.dll in the x64 stack. ANGLE worked on the affected system and v0.28.2.7 prefers ANGLE on Windows. If startup fails, update graphics drivers through the hardware vendor and capture a verbose log. Example from the extracted x64 directory in PowerShell:

```powershell
& ".\Dreamsurf x64.exe" --rendering-method gl_compatibility --rendering-driver opengl3_angle --windowed --verbose --log-file startup.txt
```

For a machine where ANGLE fails, native OpenGL can be tested with --rendering-driver opengl3, although that path crashed on the affected Intel system. Include the error, GPU and driver version in bug reports. For source imports, extract the ZIP first and import project.godot directly.

## Windows security
The previously inspected v0.28.2.7 x64 and x32 executables have no Authenticode certificate. SmartScreen may warn about publisher reputation; antivirus detections are a separate matter. Do not disable security tools. Verify the [SHA-256 checksums](SHA256SUMS.txt), scan the actual download, and report suspicious detections. Microsoft provides a [file submission portal](https://www.microsoft.com/en-us/wdsi/filesubmission) for suspected false positives. Checksums verify file identity, not safety. No independent malware scan or code signing has been completed.

For future builds, use official matching Godot templates, correct version metadata, separate EXE/PCK where practical, retain all generated DLLs and notices, and test the final archives. Trusted signing requires publisher credentials.

## Test scope
For v0.28.2.7, the developer reported successful launches; the x64 and x32 archive CRCs, PE architecture and embedded resource equivalence were independently inspected. Broader hardware validation and ARM64 runtime testing remain outstanding.

For v0.29.5.2, the source archive has been checked and its SHA-256 is listed. Final Windows exports have not yet been supplied or inspected. Do not use earlier versions' hashes to verify the new binaries.
