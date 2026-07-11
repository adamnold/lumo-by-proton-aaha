# Lumo by Proton for Linux — AAHA

Unofficial Lumo by Proton Electron desktop app for Fedora KDE, with a stable Wayland taskbar icon.

## Privacy notice

Electron is Chromium-based. The wrapper disables unnecessary background services and adds no AAHA telemetry, but Lumo, Proton Drive integrations, Proton authentication, CDNs, and deliberately selected external services still receive required traffic. It cannot promise a completely Google-free or independently auditable Chromium runtime. See PRIVACY.md.

Run ./build.sh and ./install.sh. The renamed app installs under ~/MyApps/lumo-by-proton-aaha/app. On first installation it safely copies ~/.config/Lumo to ~/.config/Lumo by Proton if needed and retains the original for rollback.

Normal uninstall preserves the new profile; ./uninstall.sh --purge removes only the new local profile. The old lumo.desktop ID remains as a hidden KDE pin compatibility launcher.

This project is unofficial and is not affiliated with Proton.
