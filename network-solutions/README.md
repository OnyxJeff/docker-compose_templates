# 💻 Netboot.xyz for Portainer

[![Docker](https://img.shields.io/badge/Docker-Netboot-blue?logo=docker)](https://hub.docker.com/r/linuxserver/netbootxyz)
[![PXE](https://img.shields.io/badge/PXE-Booting-lightgrey)](https://netboot.xyz/)

A portable PXE boot service containerized for Portainer. This stack is ideal for fast netboot installs, rescue, and sysadmin magic.

- ✅ PXE boot server
- ✅ Web interface
- ✅ DHCP proxy-ready
- ✅ Reverse proxy compatible

## 📁 File Structure
```text
network-solutions/
├── docker/             # YAML file for the network_solutions stack
└── README.md           # You're reading it!
```
---

## 🔧 Requirements
- Docker + Portainer
- Network configured to allow PXE boot clients

## 🚀 Deployment

1. In Portainer, go to Stacks > Add Stack
2. Name your stack (e.g., netbootxyz)
3. Paste in the contents of netbootxyz-stack.yml
4. Deploy and configure DHCP to point to this box

You can also clone this repo and deploy via CLI:

```bash
docker compose -f docker-compose.yml up -d
```
---

## 🌐 Access
| Service     | Port | URL                   |
|:---:        |:---: |:---:                  |
| Netboot.XYZ | 3000 | http://<your-ip>:3000 |
| NGinxRP     | 81   | http://<your-ip>:81   |

## 🔒 Reverse Proxy Setup (Optional)
If you're using NGINX Proxy Manager:
- Set domain: 'service name'.yourdomain.com
- Forward Host: 'your-local-ip'
- Forward Port: 'service port'

Enable:
- Websockets
- SSL (Let's Encrypt)
- Force HTTPS

---

## 📜 License
MIT — Because PXE should be easier.

📬 Maintained By
Jeff M. • @OnyxJeff