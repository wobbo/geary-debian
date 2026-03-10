# Geary 44.1 (arm64) for Debian 13 / Raspberry Pi OS

This repository provides a custom **Geary 44.1 ARM64 build** for **Debian 13 (Trixie)** and **Raspberry Pi OS**.

## Why this build exists

In recent Debian 13 updates, the official Geary packages (46 and 47) no longer display:

- unread message icons
- flagged message indicators
- message markers in the conversation list

This breaks the visual layout and makes Geary harder to use.

This build restores the classic behavior by providing **Geary 44.1**, where these indicators still work correctly.

More background and discussion can be found on the Raspberry Pi forum:

[geary_44.1-1wobbo1_arm64_20251202.deb](https://github.com/wobbo/geary-44.1-for-debian-trixie-arm64/raw/main/geary_44.1-1wobbo1_arm64_20251202.deb)

[HOWTO: Email Client Geary and Launches in Background on Startup (Raspberry Pi OS GNOME)](https://forums.raspberrypi.com/viewtopic.php?t=387502#p2313459)

---

# Install

Download and install the package:

```bash
t=$(mktemp -d); cd $t; wget https://github.com/wobbo/geary-44.1-arm64/releases/download/v44.1/geary_44.1-1wobbo1_arm64_20251202.deb && \
sudo apt install -y ./geary_44.1-1wobbo1_arm64_20251202.deb && sudo apt-mark hold geary; cd; rm -rf $t
