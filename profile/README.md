<div align="center">
  <h1>Realme Atoll Development</h1>
  <p><strong>Official-grade custom ROM sources, recovery trees, and Linux 4.14 kernel for Qualcomm Snapdragon 720G (SM7125) Realme devices.</strong></p>

  <p>
    <a href="https://github.com/realme-atoll"><img src="https://img.shields.io/badge/Platform-Qualcomm%20SM7125-blue?style=for-the-badge&logo=qualcomm" alt="Platform" /></a>
    <a href="https://github.com/realme-atoll/android_kernel_realme_sm7125"><img src="https://img.shields.io/badge/Kernel-Linux%204.14%20Unified-orange?style=for-the-badge&logo=linux" alt="Kernel" /></a>
    <a href="https://github.com/realme-atoll/android_device_realme_sm7125-OFRP"><img src="https://img.shields.io/badge/Recovery-OrangeFox%20R12.0-ff6600?style=for-the-badge" alt="Recovery" /></a>
  </p>
</div>

---

### Supported Devices Specifications

| Feature | Realme 6 Pro (`RMX2061`) | Realme 7 Pro (`RMX2170`) | Realme 8 Pro (`RMX3081`) |
| :--- | :---: | :---: | :---: |
| **Device Picture** | <img src="https://raw.githubusercontent.com/realme-atoll/.github/main/profile/assets/realme-6-pro.jpg" width="140" alt="Realme 6 Pro"> | <img src="https://raw.githubusercontent.com/realme-atoll/.github/main/profile/assets/realme-7-pro.jpg" width="140" alt="Realme 7 Pro"> | <img src="https://raw.githubusercontent.com/realme-atoll/.github/main/profile/assets/realme-8-pro.jpg" width="140" alt="Realme 8 Pro"> |
| **Oppo Project ID** | `19721` / `19771` | `206B1` | `20711` |
| **Chipset** | Qualcomm SM7125 Snapdragon 720G (8 nm) | Qualcomm SM7125 Snapdragon 720G (8 nm) | Qualcomm SM7125 Snapdragon 720G (8 nm) |
| **CPU** | Octa-core (2x2.3 GHz Kryo 465 Gold & 6x1.8 GHz Kryo 465 Silver) | Octa-core (2x2.3 GHz Kryo 465 Gold & 6x1.8 GHz Kryo 465 Silver) | Octa-core (2x2.3 GHz Kryo 465 Gold & 6x1.8 GHz Kryo 465 Silver) |
| **GPU** | Adreno 618 | Adreno 618 | Adreno 618 |
| **Display** | 6.6" IPS LCD (90 Hz, 1080 x 2400) | 6.4" Super AMOLED (60 Hz, 1080 x 2400) | 6.4" Super AMOLED (60 Hz, 1080 x 2400) |
| **Biometrics** | Side-Mounted Capacitive Fingerprint | In-Display Optical Fingerprint (Goodix UDFPS) | In-Display Optical Fingerprint (Goodix UDFPS) |
| **Battery & Charging** | 4300 mAh, 30W Dart Charge | 4500 mAh (Dual-cell), 65W SuperDart | 4500 mAh, 50W SuperDart |
| **Audio** | Single Bottom Speaker, Hi-Res Audio | Dual Stereo Speakers, Hi-Res Audio | Single Bottom Speaker, Hi-Res Audio |
| **Cameras** | 64 MP (Samsung GW1) + 12 MP (Tele) + 8 MP + 2 MP | 64 MP (Sony IMX682) + 8 MP (UW) + 2 MP + 2 MP | 108 MP (Samsung HM2) + 8 MP (UW) + 2 MP + 2 MP |

---

### Repository Layout

```
realme-atoll/
├── ⚙️ Unified Platform (SM7125 / Atoll)
│   ├── android_device_realme_sm7125-common    # Platform common device tree
│   ├── android_vendor_realme_sm7125-common    # Platform common vendor blobs
│   ├── android_kernel_realme_sm7125           # Linux 4.14 unified kernel source
│   ├── android_device_realme_sm7125-OFRP      # OrangeFox Recovery Project tree
│   └── crave_script                           # Automated Crave build orchestration scripts
│
├── 📱 Realme 6 Pro (RMX2061)
│   ├── android_device_realme_RMX2061          # Device-specific tree
│   ├── android_vendor_realme_RMX2061          # Proprietary vendor blobs
│   └── RMX2061-manifest                       # Local ROM build manifest
│
├── 📱 Realme 7 Pro (RMX2170)
│   ├── android_device_realme_RMX2170          # Device-specific tree
│   ├── android_vendor_realme_RMX2170          # Proprietary vendor blobs
│   └── RMX2170-manifest                       # Local ROM build manifest
│
├── 📱 Realme 8 Pro (RMX3081)
│   ├── android_device_realme_RMX3081          # Device-specific tree
│   ├── android_vendor_realme_RMX3081          # Proprietary vendor blobs
│   └── RMX3081-manifest                       # Local ROM build manifest
│
└── 🎵 Audio Enhancements
    ├── hardware_dolby                         # Dolby Atmos audio implementation
    └── packages_apps_ViPER4AndroidFX          # ViPER4AndroidFX audio effects app
```

---

### Getting Started

To sync local manifests for building AOSP / LineageOS ROMs:

```bash
# For Realme 6 Pro (RMX2061):
git clone https://github.com/realme-atoll/RMX2061-manifest.git .repo/local_manifests

# For Realme 7 Pro (RMX2170):
git clone https://github.com/realme-atoll/RMX2170-manifest.git .repo/local_manifests

# For Realme 8 Pro (RMX3081):
git clone https://github.com/realme-atoll/RMX3081-manifest.git .repo/local_manifests

# Sync all trees:
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

---

<div align="center">
  <sub>Maintained with ❤️ by <a href="https://github.com/nikhilpal2705">Nikhil Suryavanshi</a></sub>
</div>
