# Windows compatibility and distribution

## Installation
Extract the entire downloaded ZIP. Launch the EXE in the extracted folder. The supplied v0.28.2.7 Windows packages contain embedded game resources and Godot notices. Choose x64 for Intel/AMD 64-bit Windows; x32 is the 32-bit alternative. No new ARM64 package is supplied.

## Graphics
A native OpenGL crash was observed on Intel Iris Xe with igxelpicd64.dll in the x64 stack. ANGLE worked on the affected system and v0.28.2.7 prefers ANGLE on Windows. If startup fails, update graphics drivers through the hardware vendor and capture a verbose log. Example from the extracted x64 directory in PowerShell:

```powershell
& ".\Dreamsurf x64.exe" --rendering-method gl_compatibility --rendering-driver opengl3_angle --windowed --verbose --log-file startup.txt
```

For a machine where ANGLE fails, native OpenGL can be tested with --rendering-driver opengl3, although that path crashed on the affected Intel system. Include the error, GPU and driver version in bug reports. For source imports, extract the ZIP first and import project.godot directly.

## Windows security
The supplied executables have no Authenticode certificate. SmartScreen may warn about publisher reputation; antivirus detections are a separate matter. Do not disable security tools. Verify the [SHA-256 checksums](SHA256SUMS.txt), scan the actual download, and report suspicious detections. Microsoft provides a [file submission portal](https://www.microsoft.com/en-us/wdsi/filesubmission) for suspected false positives. Checksums verify file identity, not safety. No independent malware scan or code signing has been completed.

For future builds, use official matching Godot templates, correct version metadata, separate EXE/PCK where practical, retain all generated DLLs and notices, and test the final archives. Trusted signing requires publisher credentials.

## Test scope
The developer reports the updated builds work. Archive CRCs, PE architecture and embedded resource equivalence were independently inspected. Broader hardware validation and ARM64 runtime testing remain outstanding.
