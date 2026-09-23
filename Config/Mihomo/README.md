# Nikki → Core

## 全局配置

~~port: 8080~~

~~socks-port: 1080~~

~~redir-port: 7891~~

~~tproxy-port: 7892~~

## 控制面板

~~external-ui: "/etc/nikki/run/ui"~~

```yaml
external-ui: "/etc/mihomo/run/ui"
```

## 入站

~~auto-route: false~~

~~auto-redirect: false~~

~~auto-detect-interface: false~~

```yaml
auto-route: true
auto-redirect: true
auto-detect-interface: true
```

## DNS模块

~~listen: 0.0.0.0:1053~~

# Nikki → Mobile

## 全局配置

~~port: 8080~~

~~socks-port: 1080~~

~~redir-port: 7891~~

~~tproxy-port: 7892~~

## 控制面板

~~all~~

## 入站

~~auto-route: false~~

~~auto-redirect: false~~

~~auto-detect-interface: false~~

```yaml
auto-route: true
auto-detect-interface: true
```

## DNS模块

~~listen: 0.0.0.0:1053~~
