# 玩客云部署clash

## 下载crash-premium

## 设置systemd服务
```vim /etc/systemd/system/clash.service```

```
[Unit]
Description=Clash
After=network-online.target
Wants=network-online.target

[Service]
Type=simple
User=root
Execstart=/home/felix/clash-linux-armv7-2023.08.17
ExecReload=/bin/kill -s QUIT $MAINPID &/home/felix/clash-linux-armv7-2023.08.17
Execstop=/bin/kill -s QUIT $MAINPI

[Install]
WantedBy=multi-user.target
```

## 重新加载systemd服务
```systemctl daemon-reload```

## 开机启动
```systemctl enable clash```

## 启动
```systemctl start clash```

## 查看日志看是否正常启动
```systemctl status clash```
