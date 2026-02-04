🌍 Language: English | [Русский](README_RU.md)

# 🚀 Clean Russian Residential IP on Phone (No VPN Apps)

Get a **clean Russian residential IP** on your phone **without any VPN apps** installed on the device.

This method works for:
- Russian government websites
- biometrics and identity verification
- banking apps
- services with strict VPN / proxy detection

✅ No VPN on the phone  
✅ No programming  
✅ No servers to set up  
✅ Beginner-friendly  

This guide does **not** provide IP addresses or VPN services.

It explains **how to use your own trusted device in Russia** (for example, a friend’s home computer) as an internet exit point using Tailscale.

## 👤 Who is this for

- You are **outside Russia**
- You need a **real Russian residential IP**
- VPN apps are **blocked or detected** on your phone
- You need access to **government or identity-verified services**
- You want a **simple, non-technical solution**

## 🧩 How it works (short version)

- You and your trusted friend log into **the same Tailscale account**
- Your friend’s device in Russia is enabled as an **Exit Node**
- Your PC routes traffic through that Exit Node
- Your phone connects to your PC via Wi-Fi
- The phone itself has **no VPN, no proxy, no tunnel**

From the service perspective, this looks like:
> a normal phone connected to a home Russian internet connection

## 📋 Requirements

### Hardware & OS
- Windows 10 or Windows 11 PC
- **Ethernet connection** for the PC (important)
- Wi-Fi on the PC
- Android phone

### Software
- [Tailscale](https://tailscale.com)
- [MyPublicWiFi](https://mypublicwifi.com/publicwifi/en/index.html)

### Access
- A **trusted friend in Russia**
- Both of you logged into **the same Tailscale account**
- Friend’s device configured as an **Exit Node**

## 🛠️ One-time setup (friend in Russia)

1. Install **Tailscale** on the friend’s PC
2. Log in using **the same Tailscale account**
3. Enable **Run as Exit Node**
4. Confirm the device appears in Exit Nodes list

This device will act as your **Russian internet exit**.

## 🧭 Step-by-step guide (no programming)

### 1️⃣ Connect your PC via Ethernet
Wi-Fi must be free to act as a hotspot.

---

### 2️⃣ Install and start MyPublicWiFi
Run the application **as Administrator**.

Settings:
- Mode: **WLAN Hotspot**
- Network Access: **Router Mode (NAT)**
- Internet Connection: **Automatic**

⚠️ Do NOT enable Tailscale Exit Node yet.

Start the hotspot.

---

### 3️⃣ Connect your phone to the hotspot
- Connect to the Wi-Fi network created by MyPublicWiFi
- Confirm internet works on the phone

---

### 4️⃣ Enable Tailscale Exit Node (critical step)

On the PC:
- Open Tailscale tray icon
- Go to **Exit Nodes**
- Enable **Allow local network access**
- Select your friend’s **Russian Exit Node**

⚠️ Do NOT restart the hotspot.

---

### 5️⃣ Verify
- Internet on the phone continues working
- External IP is Russian
- Phone shows **no VPN, no proxy**

Done.

---

## 🧠 Why this works

- NAT and hotspot are established **before** routing changes
- Tailscale changes the default route silently
- MyPublicWiFi does not rebuild the hotspot
- The phone only sees a normal Wi-Fi network

This avoids VPN detection on the device itself.

---

## ⚠️ Limitations

- This is a Windows networking edge-case
- May break after:
  - Windows updates
  - Tailscale updates
  - network driver updates
- Ethernet connection is mandatory
- Stability depends on the PC being online

---

## 📌 Summary

This is currently one of the **simplest ways** to get a clean Russian residential IP on a phone **without installing VPN apps** and without technical setup.

---

## 📝 Disclaimer

This guide is provided for educational purposes only.  
You are responsible for complying with local laws, service terms, and regulations.

---

## 🏷️ Tags

tailscale, exit-node, residential-ip, no-vpn, hotspot, windows, android, government-sites
