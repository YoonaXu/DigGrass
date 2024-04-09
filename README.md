# 挖草
非官方挖草镜像 [getgrass.io](https://app.getgrass.io/register/?referralCode=TjuqlvK2HwffKxf)
可在Dockerhub上获得 [Docker Hub](https://hub.docker.com/r/yoonaxu/diggrass)

适配国内网络环境，预下载Grass插件，基本上配置好用户名和密码后就可以使用啦。

## 关于Grass
Grass.io 是一个基于去中心化网络资源共享平台的项目，用户通过提供自己的闲置带宽资源，可以获得Grass积分作为回报。机构利用这些资源进行市场调查、网络抓取或训练AI等任务。
由于目的并不是大量的流量传输，所以不会很消耗你的宽带流量。

## 如何操作
1. 首先注册一个帐号: [getgrass.io](https://app.getgrass.io/register/?referralCode=TjuqlvK2HwffKxf)
2. 通过Dockerfile自己源码build一个或者从DockerHub直接下载build完成的镜像。
3. 配置好自己帐号和密码，即GRASS_USER，GRASS_PASS。

### Docker执行命令
```
docker run -d \
    --name DigGrass \
    -p 8666:8666 \
    -e GRASS_USER=myuser@mail.com \
    -e GRASS_PASS=mypass \
    -e ALLOW_DEBUG=False \
    yoonaxu/diggrass
```

## 注意事项
1. 别在同一个网络跑多个帐号，多个容器，即多开。会被ban的。一条宽带最好只跑一个。
2. 你可以在网页登录你的帐号，查看你的收益和容器链接状态。
3. 容器启动后通常需要5-10min左右才能正常工作，注意观察你的Network Quality只要不是0就是正常工作，具体多少取决于你的网络环境。
