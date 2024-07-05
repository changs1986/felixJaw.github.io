# 部署zerotier

## 安装docker
```
#可选：切换国内软件源
sudo apt install docker.io
```

## 运行实例
```
docker run -d   --name zerotier --restart=always --device=/dev/net/tun --net=host --cap-add=NET_ADMIN --cap-add=SYS_ADMIN -v /var/lib/zerotier-one:/var/lib/zerotier-one bltavares/zerotier:1.10.3-arm32v7
```

## 加入网络
```
docker exec -it zerotier zerotier-cli join 网络ID
```
