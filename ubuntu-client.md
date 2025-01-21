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