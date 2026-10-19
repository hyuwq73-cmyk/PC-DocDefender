[README.txt](https://github.com/user-attachments/files/33673821/README.txt)
# PC DocDefender v0.4.0 Beta 1

**Diagnose. Detect. Defend.**

PC DocDefender is an independent, read-only Windows diagnostics and local
hash-lookup utility. It is not affiliated with Microsoft and is not a full
antivirus product.

## Run

Extract the complete `PC_DocDefender_v0.4.0_Beta_1` folder and start
`PC_DocDefender.exe`. Keep the `_internal` folder beside the executable. No
Python installation or administrator privileges are required.

## What it does

- Displays system resource and hardware information and basic diagnostics.
- Queries Microsoft Defender status and historical detections through Windows
  PowerShell when those interfaces are available.
- Computes file SHA-256 hashes and looks them up in user-maintained local data.

This beta executable does **not** bundle YARA or YARA rules. YARA is available
only in a separately prepared build with the optional `yara-python` dependency
and user-supplied, attributed rules.

The app reads scanned files only. It does not delete, quarantine, modify,
execute, upload, or automatically submit scanned files, hashes, paths, or
reports. It makes no hidden network requests and sends no telemetry. Defender
settings are never changed.

A hash match reflects only the classification and evidence in the local record.
`NO MATCH` is not proof that a file is safe. YARA matches require review. Health
Score describes configured system-condition factors; it does not measure
malware-free status.

If PowerShell, Defender, permissions, or a Windows interface is unavailable,
related information may be shown as Unknown or unavailable. This does not
confirm a threat or a clean system.

## User data

Existing databases and optional YARA rules remain in
`%LOCALAPPDATA%\PCDiagnostician\`. Reports are saved only where the user chooses.
The application bundle contains no malware or EICAR samples and no threat
database or YARA rules.

This is a beta release. Review findings with Windows Security and other trusted
tools; do not rely on PC DocDefender as the sole security control.
