# Privacy and Network Behavior

Last Updated: 2026-07-23

The wrapper adds no AAHA analytics and disables unnecessary Chromium update, background, reporting, translation, optimization, media-routing, and Secure DNS services. Known Google update/telemetry hosts are blocked.

Lumo must contact Proton service, authentication, storage, CDN, and web-search/image providers required by features the user selects. Chromium and host blocklists cannot guarantee zero Google or third-party traffic.

The active profile is ~/.config/Lumo by Proton. Installation copies the legacy ~/.config/Lumo profile only when the new profile does not exist and retains the original. Normal uninstall preserves both; --purge removes only the new configured profile.
