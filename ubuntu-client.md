# OpenVPN Setup - Ubuntu

## 1. Install OpenVPN
```bash
sudo apt update && sudo apt install openvpn
```

## 2. Connect to VPN
1. Go to your .ovpn file location:
```bash
cd /path/to/your/ovpn
```

2. Run OpenVPN:
### The .ovpn file and the auth credentials will be provided by the admins.
```bash
sudo openvpn --config your-config.ovpn
```
The system will ask for your username and password when connecting.

## Check Connection
```bash
ip addr show tun0
```
Press `Ctrl+C` to disconnect VPN.

## Enable Remote Desktop
1. Open Settings
2. Go to System > Remote Desktop
3. Enable Remote Desktop and configure your preferences

## Check Remote Desktop Status
```bash
# Check service status
systemctl status gnome-remote-desktop.service --user

# Check if service is running
ps aux | grep gnome-remote-desktop

# Restart service if needed
systemctl restart gnome-remote-desktop.service --user
```

Note: Make sure you are connected to the VPN before accepting remote connections.