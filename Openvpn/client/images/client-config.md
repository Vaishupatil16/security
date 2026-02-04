OpenVPN Client Setup Guide (Windows)
Prerequisites
A Windows client machine (Windows 10 or 11 recommended).
OpenVPN client setup files exported from the pfSense OpenVPN server.
Your OpenVPN client username and password.
<img width="1037" height="422" alt="image" src="https://github.com/user-attachments/assets/ae855c1c-2bc3-497a-8c56-b77ea4d22f0b" />

Step 1: Install OpenVPN Client on Windows
Download the OpenVPN Client for Windows from the official OpenVPN website or the link provided by your administrator.
OpenVPN Client Download

Run the OpenVPN installer .exe file.

Follow the installation wizard’s instructions and complete the installation.
<img width="711" height="551" alt="image" src="https://github.com/user-attachments/assets/d4561966-830d-4dec-9e39-5473c215ecef" />

OpenVPN Installation

Once installed, you should see the OpenVPN Client icon in your system tray (bottom-right corner of your screen).
<img width="865" height="326" alt="image" src="https://github.com/user-attachments/assets/f33d2f00-de3c-4ab0-9023-401d8bde3bea" />

OpenVPN Client Icon

Step 2: Import OpenVPN Configuration File
Obtain the OpenVPN client configuration file (usually .ovpn) exported from your pfSense OpenVPN server.
Open the OpenVPN Client application.
Click Import and select the .ovpn configuration file.
The profile will be added to your OpenVPN Client.
Step 3: Connect to the VPN
Locate the OpenVPN Client icon in the taskbar/system tray area.

Right-click on it and select the connection profile you imported.

Click Connect.

When prompted, enter your username and password provided for VPN access.
OpenVPN Login

After successful authentication, the OpenVPN client will connect, and the icon will turn green indicating an active VPN session.
OpenVPN Connected
<img width="630" height="262" alt="image" src="https://github.com/user-attachments/assets/99f543db-0e54-4122-9fd4-a662128364f6" />

Step 4: Verify VPN Connection
Open the Command Prompt (cmd).
Run the command to check your IP address:
<img width="1066" height="416" alt="image" src="https://github.com/user-attachments/assets/857992cf-84c4-4b56-b7ea-31d3d1261fe4" />

IP Configuration

You should see an IP address assigned from the VPN network (matching your pfSense LAN subnet).
Test connectivity by pinging your project LAN:
<img width="851" height="497" alt="image" src="https://github.com/user-attachments/assets/0e68947a-2b14-474f-9e0f-d7ba8cbcbda8" />


Troubleshooting Tips
Make sure the .ovpn file was imported correctly.
Verify your username and password.
Check firewall or antivirus settings that may block VPN connections.
Restart the OpenVPN Client if connection problems arise.
