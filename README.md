# Lumo by Proton for Linux — AAHA

Unofficial Lumo by Proton Electron desktop app for Fedora KDE, with a stable Wayland taskbar icon.

## Privacy notice

Electron is Chromium-based. The wrapper disables unnecessary background services and adds no AAHA telemetry, but Lumo, Proton Drive integrations, Proton authentication, CDNs, and deliberately selected external services still receive required traffic. It cannot promise a completely Google-free or independently auditable Chromium runtime. See PRIVACY.md.

Run `./build.sh` and then `./install.sh`. Direct AppImage execution creates no
installation directory. Optional integration defaults to
`~/.local/opt/aaha/lumo-by-proton-aaha`; pass
`--install-root /absolute/path/lumo-by-proton-aaha` for another per-application
root. On first installation it safely copies `~/.config/Lumo` to
`~/.config/Lumo by Proton` if needed and retains the original for rollback.

Normal uninstall preserves the new profile; `./uninstall.sh --purge` removes
only the new local profile after receipt and marker validation. The old
`lumo.desktop` ID remains as a hidden KDE pin compatibility launcher.

This project is unofficial and is not affiliated with Proton.
