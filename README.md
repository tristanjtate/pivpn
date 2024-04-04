# PiVPN with WireGuard Setup Guide

Welcome to the PiVPN setup guide with WireGuard! Follow these simple steps to set up PiVPN, a VPN server based on WireGuard, on your Raspberry Pi.

## Technologies Used:

- **PiVPN:** A simple VPN installer for Raspberry Pi.
- **WireGuard:** A modern VPN protocol known for its simplicity and security.
- **Raspberry Pi:** A versatile single-board computer used to host PiVPN.

## Items Needed:

- **Raspberry Pi:** Any model of Raspberry Pi (e.g., Raspberry Pi 3 or Raspberry Pi 4).
- **microSD Card:** A microSD card (8GB or larger) to host the PiVPN software.
- **Power Supply:** A power adapter to provide power to the Raspberry Pi.
- **Network Connection:** A local network connection (Ethernet) to connect the Raspberry Pi to your router.

## Why a VPN?

A VPN is like a secret tunnel for your internet connection. When you use a VPN, all your online activity travels through this tunnel, which is encrypted, meaning it's protected and nobody can see what you're doing.

So, why would you use it?

- Privacy: It keeps your internet browsing private. Nobody can see what websites you visit or what you do online.
- Security: It adds an extra layer of security, especially on public Wi-Fi networks, protecting your data from hackers and other bad actors.
- Access: It lets you access websites and content that might be restricted in your area, like streaming services or social media platforms.
- Anonymity: It hides your IP address, making it harder for websites and advertisers to track your online activity.
- **In short, a VPN helps keep you safe and private while you're online.**

## Steps:

1. **Prepare Raspberry Pi:**
   - Flash a fresh installation of Raspberry Pi OS Lite (Raspbian) onto the microSD card using Raspberry Pi Imager or Etcher.
   - Insert the microSD card into the Raspberry Pi and connect it to your router via Ethernet.
2. **Install PiVPN with WireGuard:**
   - Open a terminal on your Raspberry Pi or SSH into it from a remote computer.
   - Run the following command to install PiVPN with WireGuard:

     ```bash
     curl -L https://install.pivpn.io | bash
     ```

   - Follow the on-screen prompts to complete the installation process.
3. **Generate WireGuard Client Configurations:**
   - After installation, run the following command to generate WireGuard client configurations:

     ```bash
     pivpn add
     ```

   - Follow the on-screen prompts to configure the client (e.g., enter a name for the client).
4. **Download Client Configurations:**
   - Once the client configuration is generated, download it to your local machine using SCP (WinSCP) or SFTP.
   - Transfer the client configuration file (`.conf`) to your devices (e.g., computer, smartphone) that you want to connect to the VPN.
5. **Connect to VPN:**
   - Use a WireGuard client (e.g., WireGuard for Windows, WireGuard for iOS) to import the client configuration file and connect to the VPN server.
6. **Enjoy Secure Connection:**
   - Once connected, your devices will be securely connected to your Raspberry Pi VPN server, allowing you to browse the internet privately and securely.

## Troubleshooting:

- **Unable to Connect:** If you're unable to connect to the VPN, ensure that the client configuration file is correctly imported into the WireGuard client and that PiVPN with WireGuard is running correctly on your Raspberry Pi.

## Additional Resources:

- [PiVPN Documentation](https://docs.pivpn.io/)
- [PiVPN GitHub Repository](https://github.com/pivpn/pivpn)
- [WireGuard Documentation](https://www.wireguard.com/)
- [WireGuard Community Forums](https://www.reddit.com/r/WireGuard/)
