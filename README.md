# Lumo (AAHA)

A native **Lumo (by Proton) desktop app for Linux**, built with Electron
by **Adam And His Agents (AAHA)**. It wraps the official Lumo web app
(`https://lumo.proton.me`) — Proton's private AI assistant — in a clean,
standalone window that behaves like a real desktop application, including
a **stable taskbar icon that KDE Plasma on Wayland will NOT swap for the
generic browser icon**.

> **Unofficial / not affiliated with Proton.** This is a third-party
> wrapper. It is not endorsed by or affiliated with Proton AG. "Proton"
> and "Lumo" are trademarks of Proton AG. See `NOTICE` for details. Your
> use of Lumo remains subject to Proton's own Terms of Service.

---

## Why this exists

KDE on Wayland picks an app's panel icon from the window's `app_id`
(WM class) and matches it to a `.desktop` file. Chromium-based PWAs all
share Chromium's identity, so KDE falls back to the generic browser icon.

A real Electron app sets its **own** `app_id` (`app.setName()` + `--class`)
and ships a `.desktop` file whose `StartupWMClass` matches exactly.

---

## Requirements (Fedora / KDE example)

```bash
sudo dnf install nodejs npm fuse fuse-libs
```

(On Debian/Ubuntu: `sudo apt install nodejs npm libfuse2`.)

---

## Build & install

```bash
chmod +x *.sh
./build.sh
./install.sh
```

Build outputs:
- `dist/linux-unpacked/` — the native unpacked app
- `dist/*.AppImage` — a portable single-file version

To remove it later: `./uninstall.sh`

---

## Configuration (`app.config.js`)

| Field                   | Value                                            |
|-------------------------|--------------------------------------------------|
| `url`                   | `https://lumo.proton.me`                         |
| `name`                  | `Lumo`                                           |
| `wmClass`               | `Lumo`                                           |
| `appId`                 | `com.adamandhisagents.lumo`                      |
| `allowedHosts`          | `["proton.me"]` (covers Proton sign-in)          |
| `disableHardening`      | `false` (privacy hardening ON)                   |

---

## Privacy hardening (on by default)

Chromium background/phone-home subsystems are disabled by default. The
app should only talk to Proton. To opt out, set `disableHardening: true`
in `app.config.js`.

---

## License

Copyright 2026 **Adam And His Agents (AAHA)**. Wrapper code licensed
under the **Apache License, Version 2.0** — see `LICENSE`. See `NOTICE`.
