# Geary 44.1 (ARM64) for Debian 13 GNOME

This repository provides a custom **Geary 44.1 ARM64 build** for **Debian Trixie GNOME**.

The package is intended for ARM64 systems and has been **tested on Raspberry Pi 4 and Raspberry Pi 5 running Raspberry Pi OS**.

---

## Why this build exists

In recent Debian 13 GNOME updates, the official Geary packages (versions 46 and 47) no longer display:

- unread message icons
- flagged message indicators
- message markers in the conversation list

![Geary screenshot](https://wobbo.org/screenshots/20250225__373028_Geary_009.webp)

This breaks the visual layout and makes Geary harder to use.

This build restores the classic behavior by providing **Geary 44.1**, where these indicators still work correctly.

More background and discussion can be found on the Raspberry Pi forum:

- [HOWTO: Email Client Geary and Launches in Background on Startup (Raspberry Pi OS GNOME)](https://forums.raspberrypi.com/viewtopic.php?t=387502#p2313459)

---

## Package

Download the ARM64 package:

[geary_44.1-1wobbo1_arm64_20251202.deb](https://github.com/wobbo/geary-44.1-for-debian-trixie-arm64/releases/download/v44.1/geary_44.1-1wobbo1_arm64_20251202.deb)

---

# Install

Download and install the package:

```bash
t=$(mktemp -d); cd $t; wget https://github.com/wobbo/geary-44.1-arm64/releases/download/v44.1/geary_44.1-1wobbo1_arm64_20251202.deb && \
sudo apt install -y ./geary_44.1-1wobbo1_arm64_20251202.deb && sudo apt-mark hold geary; cd; rm -rf $t
