# Momo → Core

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

~~{"type": "logical", "mode": "or", "rules": [{"domain_suffix": "push.apple.com"}, {"rule_set": "geoip-telegram"}], "invert": true, "action": "sniff", "sniffer": ["http", "tls", "stun", "quic", "dns"], "timeout": "200ms"},~~

~~{"inbound": "dns-in", "action": "hijack-dns"},~~

```json
      {"type": "logical", "mode": "and", "rules": [{"port": [53, 853], "invert": true}, {"clash_mode": "Global", "invert": true}, {"type": "logical", "mode": "or", "rules": [{"ip_is_private": true}, {"rule_set": "geoip-cn"}]}], "action": "bypass"},
      {"type": "logical", "mode": "or", "rules": [{"domain_suffix": "push.apple.com"}, {"rule_set": "geoip-telegram"}], "invert": true, "action": "sniff", "sniffer": ["http", "tls", "stun", "quic", "dns"], "timeout": "200ms"},
      {"type": "logical", "mode": "or", "rules": [{"port": 53}, {"protocol": "dns"}], "action": "hijack-dns"},
```

~~{"action": "resolve"},~~

```json
      {"inbound": "mixed-in", "action": "resolve"},
```

~~"auto_detect_interface": false~~

```json
    "auto_detect_interface": true
```

# Momo → PC

## experimental

~~all~~

```json
  "experimental": {
    "cache_file": {
      "enabled": true,
      "store_dns": true
    }
  },
```

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
      "platform": {
        "http_proxy": {
          "enabled": true,
          "server": "127.0.0.1",
          "server_port": 7890
        }
      }
    },
    {
      "tag": "mixed-in",
      "type": "mixed",
      "listen": "0.0.0.0",
      "listen_port": 7890
    }
  ],
```

## outbounds

```json
    {"tag": "Bridge","type": "bridge"},
```

## route

~~{"type": "logical", "mode": "or", "rules": [{"domain_suffix": "push.apple.com"}, {"rule_set": "geoip-telegram"}], "invert": true, "action": "sniff", "sniffer": ["http", "tls", "stun", "quic", "dns"], "timeout": "200ms"},~~

~~{"inbound": "dns-in", "action": "hijack-dns"},~~

```json
      {"type": "logical", "mode": "and", "rules": [{"port": [53, 853], "invert": true}, {"clash_mode": "Global", "invert": true}, {"preferred_by": ["Bridge"]}, {"type": "logical", "mode": "or", "rules": [{"ip_is_private": true}, {"rule_set": "geoip-cn"}]}], "outbound": "Bridge"},
      {"type": "logical", "mode": "or", "rules": [{"domain_suffix": "push.apple.com"}, {"rule_set": "geoip-telegram"}], "invert": true, "action": "sniff", "sniffer": ["http", "tls", "stun", "quic", "dns"], "timeout": "200ms"},
      {"type": "logical", "mode": "or", "rules": [{"port": 53}, {"protocol": "dns"}], "action": "hijack-dns"},
```

~~{"action": "resolve"},~~

```json
      {"inbound": "mixed-in", "action": "resolve"},
```

~~"auto_detect_interface": false~~

```json
    "auto_detect_interface": true
```

# Momo → Mobile

## experimental

~~all~~

```json
  "experimental": {
    "cache_file": {
      "enabled": true
    }
  },
```

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
      "platform": {
        "http_proxy": {
          "enabled": true,
          "server": "127.0.0.1",
          "server_port": 7890
        }
      }
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

~~{"inbound": "dns-in", "action": "hijack-dns"},~~

```json
      {"type": "logical", "mode": "or", "rules": [{"port": 53}, {"protocol": "dns"}], "action": "hijack-dns"},
```

~~{"action": "resolve"},~~

```json
      {"inbound": "mixed-in", "action": "resolve"},
```

~~"auto_detect_interface": false~~

```json
    "auto_detect_interface": true
```
