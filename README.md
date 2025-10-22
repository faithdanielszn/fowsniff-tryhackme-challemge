# fowsniff-tryhackme-challemge
a practical showcase of network enumeration, service fingerprinting, and exploiting weak authentication skills
---

## 🧠 Overview

This walkthrough documents the **Fowsniff** room on [TryHackMe](https://tryhackme.com/), focusing on enumeration, exploitation, and privilege escalation techniques used to compromise the vulnerable machine.

I enumerated open services like FTP and POP3, harvested credentials and files, used recovered credentials to pivot to SSH where possible, and performed privilege escalation to capture the root flag. This walkthrough records the commands I ran, findings, screenshots, and lessons learned for reproducible learning.

# Step 1 — Connect to TryHackMe (OpenVPN)

## Files & Preparation

1. **Download the .ovpn File**:
   - Navigate to the TryHackMe Access (or VPN) page and download the .ovpn file.

2. **Store the File**:
   - Place the .ovpn file in a convenient location, such as `~/vpn/tryhackme.ovpn`, for easy access when importing or running it.

## What This Does

- The OpenVPN profile establishes a secure tunnel between your machine and the TryHackMe lab network.

- **Keep the VPN Connection Active**: Ensure the VPN connection remains active for the entire duration of your engagement. Closing it will disconnect you from the lab machines.

## Verifying the Connection

1. **Check for VPN Interface**:
   - Verify that a VPN/tunnel network interface appears on your system, commonly named `tun0` or similar.

2. **Confirm Public IP**:
   - Ensure your public IP or routed address differs from your normal ISP-assigned IP, indicating that traffic is routed through the VPN.

3. **Test Connectivity**:
   - Test basic connectivity to the target machine specified in the room to ensure packets are reaching the lab.

## Notes / Tips

- **Using a GUI**:
  - If you prefer a graphical user interface, import the .ovpn file into your OS network manager (GNOME/KDE) and connect from the network menu.

- **Authentication Issues**:
  - If the VPN fails to authenticate or connect, re-download the .ovpn file from the TryHackMe Access page, as profiles can be user-specific or expire.

- **Maintain VPN Connection**:
  - Keep the VPN running throughout the exercise; it is required to access TryHackMe machines.****

