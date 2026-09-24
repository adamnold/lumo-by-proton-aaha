# Changelog

Last Updated: 2026-09-24

## v2.2.0 — 2026-09-24

- Updated from exact Electron 43.1.0 to exact Electron 44.4.5 (Chromium
  security fixes); no application source, security policy, or profile changes
  were needed for the Electron 44 breaking changes.
- Refreshed the locked build tooling to clear every `npm audit` finding,
  including the `brace-expansion`, `tar`, `undici`, and `js-yaml` advisories
  that had begun failing the required CI audit step on `master`.
- Added a manual-only Release workflow that builds the AppImage from the
  draft release's target commit, attaches it with `SHA256SUMS`, and publishes
  the draft. CI validation builds remain non-publishing.
- Supersedes the unmerged Copilot Electron 44.3.0 draft.

## v2.1.0 — 2026-07-23

- Reconciled documentation dates and corrected the bundled icon source path.
- Restored the regular Lumo by Proton description on the hidden compatibility
  launcher while preserving its stable KDE panel identity and hidden status.
- Made validation builds explicitly non-publishing, added regression coverage,
  and upgraded the GitHub Actions runtimes used by CI.
- Updated the locked build dependency tree to use the patched `fast-uri` 3.1.4
  release.

## v2.0.1 — 2026-07-15

- Added the standard `~/.local/opt/aaha/lumo-by-proton-aaha` default and
  explicit custom-root installation without changing AppImage execution.
- Added guarded installation receipts, identity markers, and regression tests
  for unsafe paths, mismatches, profile preservation, and purge.
- Made icon generation deterministic by removing variable PNG metadata.

## v2.0.0 — 2026-07-11

- Renamed the repository, product, executable, AppImage, app ID, icon, install folder, and active profile to Lumo by Proton.
- Added a safe copied-profile migration and hidden lumo.desktop compatibility launcher.
- Updated Electron 31 to exact Electron 43.1.0 with the AAHA v2 security, privacy, build, test, checksum, and installer standard.

## v1.0.0

- Initial Lumo wrapper. Superseded by the renamed v2 release and unsupported Electron runtime.
