ss_ap - create AP with shadowsocks relay use Docker for RPi3
===

> tested on RPi3 Raspbian Lite, not support HypriotOS

```
_________________________________________
/ create an AP with shadowsocks relay use \
\ Docker                                  /
-----------------------------------------
   \
	\
	 \
				   ##         .
			 ## ## ##        ==
		  ## ## ## ## ##    ===
	  /"""""""""""""""""\___/ ===
	 {                       /  ===-
	  \______ O           __/
		\    \         __/
		 \____\_______/


```

### TAGS

2.5.6, arm 

[![](https://images.microbadger.com/badges/image/yangxuan8282/ss_ap.svg)](https://microbadger.com/images/yangxuan8282/ss_ap "Get your own image badge on microbadger.com")

amd64, 2.5.6-amd64

[![](https://images.microbadger.com/badges/image/yangxuan8282/ss_ap:amd64.svg)](https://microbadger.com/images/yangxuan8282/ss_ap:amd64 "Get your own image badge on microbadger.com")

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
