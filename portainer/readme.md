# docker 容器管理

## 注意点

- 需要docker开启外网连接端口，默认为2375

  - 编辑文件
    vi /usr/lib/systemd/system/docker.service

  - 追加
    找到 ExecStart=ExecStart=/usr/bin/dockerd 后面追加 -H tcp://0.0.0.0:2375 -H unix://var/run/docker.sock

  - 重启docker
    systemctl daemon-reload
    systemctl restart docker
