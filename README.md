# HTPC Download Box

All credit to https://github.com/sebgl/htpc-download-box

## Setup (Ubuntu)

```
sudo apt-get update
```

```
sudo apt-get install git docker docker-compose -y
```

```
sudo systemctl enable docker && systemctl start docker
```

```
sudo groupadd docker
```

```
sudo usermod -aG docker $USER
```

## Portainer

Optional, but Portainer allows ease of access/monitoring/administrating of each container and your whole stack:

- Install Portainer: https://docs.portainer.io/start/install-ce/server/docker/linux
- Create a stack (e.g. `media-server`)
- Paste the contents of `docker-compose.yml` into the editor
- Add the contents of your .env as environment vars (going into advanced mode will allow you to paste the contents of `.env` vs adding one at a time)
- Launch stack

## VPN

This project uses NordVPN as the connection type for the `transmission-openvpn` container, but many others are available. See: https://haugene.github.io/docker-transmission-openvpn/

If you are using NordVPN, use the encrypted username/password available via their portal for setup on routers/otherdevices