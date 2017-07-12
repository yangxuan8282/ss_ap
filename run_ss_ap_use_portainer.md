> `docker` 的安装可以参照这里： https://yangxuan8282.github.io/pi-notes/#!docker.md

首先启动一个 `portainer` 容器：

```
docker run -d --restart=always -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock --name Portainer portainer/portainer:linux-arm
```

> amd64 的话就用 `portainer/portainer:linux-amd64` 这个镜像

然后通过 IP:9000 访问 portainer，树莓派的话可以通过 http://raspberrypi:9000 来访问

1.点击首页既 dashboard 页面的 `Containers`，也可以点击左侧第四个图标进入

![](https://i.imgur.com/6ye9zwV.png)

2.添加容器

![](https://i.imgur.com/bllmLXm.png)

3.分别输入容器名称和镜像名称

![](https://i.imgur.com/FMM5qYY.png)

> amd64 使用 `yangxuan8282/ss_ap:amd64` 这个镜像

4.选择网络模式

![](https://i.imgur.com/8tICTYp.png)

5.填入自己的无线热点及 ss 服务器信息

![](https://i.imgur.com/VTjLhL7.png)

6.选择重启策略

![](https://i.imgur.com/KVpndJi.png)

7.启用 privileged mode

![](https://i.imgur.com/TkkA2iw.png)

8.启动容器

![](https://i.imgur.com/Abyissx.png)

9.点击进入刚才建立的容器，这个页面有 `stats`, `logs` 和 `console` 分别可以查看容器占用的资源及进程，容器日志以及通过 sh/bash 连接到容器内

![](https://i.imgur.com/dKtjKvO.png)
