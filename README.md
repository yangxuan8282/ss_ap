ss_ap - create AP with shadowsocks relay use Docker for RPi3
===

> tested on RPi3 Raspbian Lite, not support HypriotOS

### FROM

[oblique/create_ap](https://github.com/oblique/create_ap)

[shadowsocks-libev](https://github.com/shadowsocks/shadowsocks-libev)

### Docker Compose

[docker-compose.yml](./docker-compose/docker-compose.yml)

> `create_ap` will take 100% of 1 core on Raspberry Pi 3

### stop

```
docker-compose stop -t 30
```

> `create_ap` is slow in container, need give it more time to finish cleanup (iptables rule)

```
docker-compose down
```
