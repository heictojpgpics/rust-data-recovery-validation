# Rust Data Recovery Wizard — Validation

This repo contains validation workflows for the [`rust-data-recovery-wizard`](https://github.com/heictojpgpics/rust-data-recovery-wizard) project.

## What this repo does

- Provides Windows GitHub Actions runners that:
  1. Build the main project (RDW) from source.
  2. Generate or download fixture disk images (NTFS, FAT32, exFAT) with known contents.
  3. Run the RDW binary against each fixture.
  4. Assert that all expected files are recovered.
  5. Upload build artifacts + scan logs for further analysis.

## Workflows

- [`validate-windows.yml`](.github/workflows/validate-windows.yml) — Runs on every push to the main RDW repo. Builds RDW, generates fixtures, scans, validates.

## Fixtures

Fixture disk images live in `fixtures/`. Each is a small (1-10 MB) disk image with known files written to it. Generation scripts live in `scripts/`.

## Relationship to the main repo

This repo is triggered by:
1. Pushes to `heictojpgpics/rust-data-recovery-wizard` (via `repository_dispatch`)
2. Manual `workflow_dispatch` triggers

It does NOT contain the main RDW source — that lives in the main repo.
