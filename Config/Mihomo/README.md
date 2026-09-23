# Nikki → Core

- 全局配置

~~port: 8080~~

~~socks-port: 1080~~

~~redir-port: 7891~~

~~tproxy-port: 7892~~

- 控制面板

~~external-ui: "/etc/nikki/run/ui"~~

external-ui: "/etc/mihomo/run/ui"

- 入站

~~auto-route: false
auto-redirect: false
auto-detect-interface: false~~

auto-route: true
auto-redirect: true
auto-detect-interface: true

- DNS模块

~~listen: 0.0.0.0:1053~~

# Nikki → Mobile

- 全局配置

~~port: 8080
socks-port: 1080
redir-port: 7891
tproxy-port: 7892~~

- 控制面板

~~external-controller: 0.0.0.0:9090
external-ui: "/etc/nikki/run/ui"
external-ui-name: zashboard
external-ui-url: "https://github.com/Zephyruso/zashboard/releases/latest/download/dist.zip"
secret: ""~~

- 入站

~~auto-route: false
auto-redirect: false
auto-detect-interface: false~~

auto-route: true
auto-detect-interface: true

- DNS模块

~~listen: 0.0.0.0:1053~~



