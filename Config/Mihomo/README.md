# Nikki → Core

~~port: 8080~~

~~socks-port: 1080~~

~~redir-port: 7891~~

~~tproxy-port: 7892~~

## tun

~~auto-route: false~~

~~auto-redirect: false~~

~~auto-detect-interface: false~~

```yaml
  auto-route: true
  auto-redirect: true
  auto-detect-interface: true
  route-exclude-address-set:
    - cn_ip
```

## dns

~~listen: 0.0.0.0:1053~~

# Nikki → PC

~~port: 8080~~

~~socks-port: 1080~~

~~redir-port: 7891~~

~~tproxy-port: 7892~~

## external

~~all~~

## tun

~~auto-route: false~~

~~auto-redirect: false~~

~~auto-detect-interface: false~~

```yaml
  auto-route: true
  auto-detect-interface: true
```

## dns

~~listen: 0.0.0.0:1053~~

# Nikki → Mobile

同 Nikki → PC
