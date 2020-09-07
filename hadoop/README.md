# docker

## 启动

```bash
  docker-compose up -d
```

## 访问

- Namenode: http://<dockerhadoop_IP_address>:9870/dfshealth.html#tab-overview
- History server: http://<dockerhadoop_IP_address>:8188/applicationhistory
- Datanode: http://<dockerhadoop_IP_address>:9864/
- Nodemanager: http://<dockerhadoop_IP_address>:8042/node
- Resource manager: http://<dockerhadoop_IP_address>:8088/

## 修改
打开宿主机(namenode和datanode必须在同一个网段,在window中无法使用，必须部署到Linux下)

```bash
  vi /etc/hosts

  # 追加
  <namenode 容器内部ip> namenode

  reboot
```