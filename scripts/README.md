# Scripts

Fixture generation + validation scripts live here.

## Planned scripts

- `generate-ntfs-fixture.ps1` — Create an NTFS VHD with known files.
- `generate-fat32-fixture.ps1` — Create a FAT32 VHD with known files.
- `generate-exfat-fixture.ps1` — Create an exFAT VHD with known files.
- `validate-recovery.ps1` — Run RDW against a fixture, assert all expected files recovered.
- `generate-corrupt-fixture.ps1` — Take a clean fixture and corrupt specific sectors (to test recovery of damaged volumes).
