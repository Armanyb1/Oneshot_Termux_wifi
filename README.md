<div align="center">

# 🚀 ONESHOT TERMUX [PRO EDITION] 🚀
### *Next-Gen Advanced Wi-Fi WPS Security & Penetration Testing Framework for Android*

[![GitHub release](https://img.shields.io/badge/Release-v1.0.1%20PRO-blue?style=for-the-badge&logo=github)](https://github.com/ArmanYB/OneShot-Termux)
[![Platform](https://img.shields.io/badge/Platform-Termux%20%2F%20Android-green?style=for-the-badge&logo=android)](https://termux.dev)
[![Security](https://img.shields.io/badge/Security-Root%20Required-red?style=for-the-badge&logo=linux)](https://github.com)
[![Developer](https://img.shields.io/badge/Developer-Arman%20YB-purple?style=for-the-badge)](https://github.com/ArmanYB)

</div>

---

> **⚠️ DISCLAIMER / সতর্কবার্তা:** This tool is strictly developed for educational purposes and authorized security testing. এই টুলটি শুধুমাত্র শিক্ষামূলক এবং অনুমোদিত সিকিউরিটি টেস্ট করার জন্য তৈরি করা হয়েছে। Use only on networks you own or have explicit permission to test.

---

## 🌟 Overview / সংক্ষিপ্ত পরিচিতি
**OneShot Termux (Pro Edition)** is an elite implementation of the renowned [OneShot](https://github.com/drygdryg/OneShot) toolkit, custom-engineered for **Termux** via a `.deb` package. 
এটি Termux-এর জন্য তৈরি করা একটি এডভান্সড Wi-Fi WPS পিন অ্যাটাক টুল, যার মাধ্যমে সহজে কাজ করা যায়।

---

## ✨ Core Features / মূল বৈশিষ্ট্যসমূহ
- ⚡ **Pixie Dust Attack:** Offline WPS vulnerability exploitation (অফলাইন এক্সপ্লয়েট).
- 🌐 **3WiFi Integration:** Built-in offline WPS PIN generator support (বিল্ট-ইন জেনারেটর).
- 🔓 **Online Brute-Force:** High-speed active online PIN testing (অনলাইন ব্রুটফোর্স).
- 📶 **Smart Wi-Fi Scanner:** Network scanning and highlighting based on `iw` (স্মার্ট ওয়াইফাই স্ক্যানার).

---

## 🛠️ Installation Guide / ইনস্টলেশন গাইড
Follow these steps in your Termux terminal. Make sure your device has **Root access**.
টার্মিনালে নিচের কমান্ডগুলো দিয়ে খুব সহজেই ইন্সটল করে নাও (রুট এক্সেস থাকতে হবে):

### Step 1: Update & Repositories / আপডেট এবং রিপোজিটরি সেটআপ
```bash
pkg update -y && pkg upgrade -y
pkg install wget root-repo openssl -y
```

### Step 2: Runtime Dependencies / প্রয়োজনীয় টুলস ইন্সটল
```bash
pkg install python wireless-tools iw wpa-supplicant -y
```

### Step 3: Package Installation / প্যাকেজ ইন্সটলেশন
```bash
wget https://github.com/ArmanYB/OneShot-Termux/releases/download/v1.0.1/oneshot.deb
pkg install ./oneshot.deb
```

---

## 📖 Usage & Arguments / ব্যবহারের নিয়ম ও কমান্ড
```text
OneShotPin Pro 1.0.1 (c) 2026 Arman YB
oneshot <arguments>
```

### 📌 Required Arguments / প্রয়োজনীয় আর্গুমেন্ট
* `-i, --interface=<wlan0>` — Specify the active wireless network interface (ওয়াইফাই ইন্টারফেসের নাম).

### 📌 Optional Arguments / ঐচ্ছিক আর্গুমেন্ট
* `-b, --bssid=<mac>` — Target Access Point BSSID address (টার্গেট ওয়াইফাইর বিএসআইডি).
* `-p, --pin=<wps pin>` — Use a custom WPS PIN (কাস্টম ডব্লিউপিএস পিন).
* `-K, --pixie-dust` — Run offline Pixie Dust attack (পিক্সি ডাস্ট অ্যাটাক রান করতে).
* `-B, --bruteforce` — Run online active brute-force attack (অনলাইন ব্রুটফোর্স).

### 📌 Advanced Arguments / এডভান্সড আর্গুমেন্ট
* `-d, --delay=<n>` — Set delay between pin attempts (চেষ্টার মাঝে বিরতি).
* `-w, --write` — Save AP credentials to file on success (সফল হলে ফাইল সেভ হবে).
* `-F, --pixie-force` — Run Pixiewps with `--force` flag (ফোর্স মোড).
* `--iface-down` — Bring network interface down when finished (কাজ শেষে ইন্টারফেস বন্ধ করা).
* `-l, --loop` — Run in a continuous loop (লুপ আকারে চালানো).
* `-v, --verbose` — Verbose output mode (বিস্তারিত তথ্য দেখা).
* `-m, --mtk-fix` — MediaTek chipset fix (মিডিয়াটেক ফিক্স).

---

## 💡 Practical Examples / ব্যবহারের উদাহরণ

### 🎯 Target Specific Network / নির্দিষ্ট নেটওয়ার্কে পিক্সি ডাস্ট অ্যাটাক:
```bash
sudo oneshot -i wlan0 -b 00:90:4C:C1:AC:21 -K
```

### 🔍 Scan & Auto-Attack / স্ক্যান করে অটো অ্যাটাক শুরু করতে:
```bash
sudo oneshot -i wlan0 -K
```

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
