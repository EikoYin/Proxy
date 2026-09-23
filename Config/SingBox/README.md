# Momo → Core

## experimental

~~"external_ui": "/etc/momo/run/ui"~~

~~"path": "/etc/momo/run/cache.db"~~

"external_ui": "/etc/sing-box/run/ui"

"path": "/etc/sing-box/run/cache.db"

## inbounds

~~all~~

```json
  "inbounds": [
    {
      "tag": "tun-in",
      "type": "tun",
      "address": [
        "172.18.0.1/30",
        "fdfe:dcba:9876::1/126"
      ],
      "stack": "mixed",
      "auto_route": true,
      "auto_redirect": true
    },
    {
	  "tag": "mixed-in",
      "type": "mixed",
      "listen": "0.0.0.0",
      "listen_port": 7890
    }
  ],
```

## route

~~"auto_detect_interface": false~~

"auto_detect_interface": true

# Momo → Mobile

## experimental

~~"external_controller": "0.0.0.0:9090"~~

~~"external_ui": "/etc/momo/run/ui"~~

~~"external_ui_download_url": "https://github.com/Zephyruso/zashboard/releases/latest/download/dist.zip"~~

~~"secret": ""~~

~~"path": "/etc/momo/run/cache.db"~~

## inbounds

~~all~~

```json
  "inbounds": [
    {
      "tag": "tun-in",
      "type": "tun",
      "address": [
        "172.18.0.1/30",
        "fdfe:dcba:9876::1/126"
      ],
      "stack": "mixed",
      "auto_route": true
    },
    {
	 "tag": "mixed-in",
      "type": "mixed",
      "listen": "127.0.0.1",
      "listen_port": 7890
    }
  ],
```

## route

~~"auto_detect_interface": false~~

"auto_detect_interface": true



