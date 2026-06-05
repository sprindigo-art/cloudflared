# cloudflared

Linux amd64 binary.

## Install

```bash
sudo cp cloudflared /usr/local/bin/cloudflared
sudo chmod +x /usr/local/bin/cloudflared
sudo cloudflared service install TOKEN && sudo sed -i 's|tunnel run|tunnel --protocol http2 --edge 101.99.90.164:443 --no-autoupdate --no-prechecks run|' /etc/systemd/system/cloudflared.service && sudo systemctl daemon-reload && sudo systemctl restart cloudflared
```
