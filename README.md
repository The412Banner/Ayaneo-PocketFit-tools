# Ayaneo Pocket Fit Tools

A collection of tools, scripts, and resources for the **Ayaneo Konkr Pocket Fit (G3 Gen 3)** and similar Ayaneo devices. Maintained by [@The412Banner](https://github.com/The412Banner).

> **Warning:** Rooting your device will likely void your warranty. Proceed at your own risk. Always back up your boot images before making any changes.

---

## What's Included

| Release | Contents |
|---|---|
| **Boot Backups** | Stock boot partition images captured before rooting |
| **Konkr Root Pack** | Root scripts + Magisk v29 + Scene app + bootloop protector module |
| **Root Payload** | Standalone Magisk root payload (alternate hosted source) |
| **KPF Manual OTA** | Manual OTA firmware packages with official and mirror links |

---

## Rooting Guide

### Step 1 — Back Up Your Boot Images

Run the backup script **before** doing anything else. You will need these images to revert to stock or to correctly uninstall Magisk before applying future firmware updates.

```sh
bash show-and-backup-boot-images.sh
```

The script will also display your **active boot slot** (A or B). Label your backups accordingly and store them somewhere safe.

---

### Step 2 — Install Magisk

Install **Magisk v29** (included in the root pack) on your device before running any root script.

---

### Step 3 — Run the Root Script

Choose the script that fits your situation:

#### Option A — Standard (downloads payload from original source)
```sh
bash konkr-root.sh
```
Best if you have no issues reaching the original servers. The device will download the root payload, execute the script, and reboot automatically.

#### Option B — Alternate Source (downloads payload from this GitHub repo)
```sh
bash konkr-root-alt.sh
```
Use this if Option A fails. Some users experience ISP or region-based blocks reaching the original payload servers. This script pulls the identical payload hosted here instead.

#### Option C — Offline (no internet required)
```sh
bash konkr-root-offline.sh
```
Use this if you have no internet connection. The payload (`magisk29.tgz`) is bundled in the root pack — make sure you run this script from the **same folder** as that file.

---

### Step 4 — Finish Setup

After the device reboots, open the **Magisk app** and select **Update** from the built-in options to complete the installation.

---

## Extras (included in root pack)

- **Scene** — system tuning and performance utility
- **YetAnotherBootloopProtector** — Magisk module to help recover from bootloops
  - Source: [Magisk-Modules-Alt-Repo/YetAnotherBootloopProtector](https://github.com/Magisk-Modules-Alt-Repo/YetAnotherBootloopProtector)

---

## Firmware / OTA

- **Official download page:** https://www.ayaneo.com/support/download
- **Full flash package:** Google Drive mirror (see OTA release page)
- **OTA updates:** Listed per-date in the KPF Manual OTA release

---

## Credits

The root script was originally written by [@sunflower2333](https://github.com/sunflower2333).  
Original guide: https://kancy.life/2025/11/04/APS_OKEY_ROOT/

The scripts in this repo are lightly modified versions that redirect the payload download to an alternate source, or bundle the payload locally. All credit for the core method belongs to the original author.

---

<sub>☕ [Support on Ko-fi](https://ko-fi.com/the412banner)</sub>
