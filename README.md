<div align="center">

# 🚀 ONESHOT TERMUX [PRO EDITION] 🚀
### *Next-Gen Advanced Wi-Fi WPS Security & Penetration Testing Framework for Android*

[![GitHub release](https://img.shields.io/badge/Release-v3.0.0%20PRO-blue?style=for-the-badge&logo=github)](https://github.com/ArmanYB/Oneshot_Termux_wifi/releases)
[![Platform](https://img.shields.io/badge/Platform-Termux%20%2F%20Android-green?style=for-the-badge&logo=android)](https://termux.dev)
[![Security](https://img.shields.io/badge/Security-Root%20Required-red?style=for-the-badge&logo=linux)](https://github.com)
[![Developer](https://img.shields.io/badge/Developer-Arman%20YB-purple?style=for-the-badge)](https://github.com/ArmanYB)

</div>

---

> **⚠️ DISCLAIMER / সতর্কবার্তা:** This tool is strictly developed for educational purposes and authorized security testing. এই টুলটি শুধুমাত্র শিক্ষামূলক এবং অনুমোদিত সিকিউরিটি টেস্ট করার জন্য তৈরি করা হয়েছে। Use only on networks you own or have explicit permission to test.

---

## 🌟 Overview / সংক্ষিপ্ত পরিচিতি
**OneShot Termux (Pro Edition)** is an elite implementation of the renowned [OneShot](https://github.com/drygdryg/OneShot) toolkit, custom-engineered for **Termux** via a `.deb` package. 
এটি Termux-এর জন্য তৈরি করা একটি এডভান্সড Wi-Fi WPS পিন অ্যাটাক টুল, যার মাধ্যমে খুব সহজেই কাজ করা যায়।

---

## ✨ Core Features / মূল বৈশিষ্ট্যসমূহ
- ⚡ **Pixie Dust Attack:** Offline WPS vulnerability exploitation (অফলাইন এক্সপ্লয়েট).
- 🌐 **3WiFi Integration:** Built-in offline WPS PIN generator support (বিল্ট-ইন জেনারেটর).
- 🔓 **Online Brute-Force:** High-speed active online PIN testing (অনলাইন ব্রুটফোর্স).
- 📶 **Smart Wi-Fi Scanner:** Network scanning and highlighting based on `iw` (স্মার্ট ওয়াইফাই স্ক্যানার).

---

## ⚡ Master Command Center / সকল কমান্ড এক নজরে
ইনস্টলেশন থেকে শুরু করে টুলস রান করার সমস্ত কমান্ড নিচে একত্রে দেওয়া হলো:

### 1️⃣ Installation Commands (ইনস্টলেশন কমান্ডসমূহ)
```bash
# Update repositories and install dependencies
pkg update -y && pkg upgrade -y
pkg install wget root-repo openssl python wireless-tools iw wpa-supplicant -y

# Download and install OneShot deb package (v3.0.0-PRO)
wget https://github.com/ArmanYB/Oneshot_Termux_wifi/releases/download/v3.0.0-PRO/oneshot.deb
pkg install ./oneshot.deb
```

### 2️⃣ Execution & Usage Commands (রানিং কমান্ডসমূহ)
```text
OneShotPin Pro 3.0.0-PRO (c) 2026 Arman YB
oneshot <arguments>
```

* **Target Specific Network via Pixie Dust (নির্দিষ্ট নেটওয়ার্কে অ্যাটাক):**
  ```bash
  sudo oneshot -i wlan0 -b 00:90:4C:C1:AC:21 -K
  ```

* **Scan & Auto-Attack (স্ক্যান করে অটো অ্যাটাক):**
  ```bash
  sudo oneshot -i wlan0 -K
  ```

---

## 📖 Command Arguments Reference / কমান্ড আর্গুমেন্ট বিবরণ
* `-i, --interface=<wlan0>` — Specify active wireless interface (ওয়াইফাই ইন্টারফেসের নাম).
* `-b, --bssid=<mac>` — Target Access Point BSSID address (টার্গেট ওয়াইফাইর বিএসআইডি).
* `-p, --pin=<wps pin>` — Use a custom WPS PIN (কাস্টম ডব্লিউপিএস পিন).
* `-K, --pixie-dust` — Run offline Pixie Dust attack (পিক্সি ডাস্ট অ্যাটাক).
* `-B, --bruteforce` — Run online active brute-force attack (অনলাইন ব্রুটফোর্স).
* `-d, --delay=<n>` — Set delay between pin attempts (চেষ্টার মাঝে বিরতি).
* `-w, --write` — Save AP credentials to file on success (সফল হলে ফাইল সেভ হবে).
* `-F, --pixie-force` — Run Pixiewps with `--force` flag (ফোর্স মোড).
* `--iface-down` — Bring network interface down when finished (ইন্টারফেস বন্ধ করা).
* `-l, --loop` — Run in a continuous loop (লুপ আকারে চালানো).
* `-v, --verbose` — Verbose output mode (বিস্তারিত তথ্য দেখা).
* `-m, --mtk-fix` — MediaTek chipset fix (মিডিয়াটেক ফিক্স).

---

## 🔧 Troubleshooting / সমস্যা সমাধান

### ❌ Issue 1: "RTNETLINK answers: Operation not possible due to RF-kill"
* **Solution / সমাধান:** Run the unblock command:
  ```bash
  sudo rfkill unblock wifi
  ```

### ❌ Issue 2: "Device or resource busy (-16)"
* **Solution / সমাধান:** Turn off Wi-Fi in system settings manually or use `--iface-down`.

---

## 🏆 Credits & Developer / ডেভেলপার তথ্য
* **Developer / ডেভেলপার:** **`Arman YB`**
