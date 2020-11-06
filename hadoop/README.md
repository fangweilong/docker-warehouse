# docker

## 启动

```bash
  docker-compose up -d
```

## 一些说明

- hadoop会返回hostname

## 访问

- Namenode: http://<dockerhadoop_IP_address>:9870/dfshealth.html#tab-overview

- History server: http://<dockerhadoop_IP_address>:8188/applicationhistory

- Datanode: http://<dockerhadoop_IP_address>:9864/

- Nodemanager: http://<dockerhadoop_IP_address>:8042/node

- Resource manager: http://<dockerhadoop_IP_address>:8088/

## 外部访问hdfs

- 更改host

  - 通过docker ps找到datanode的容器id

  - 编辑本机的hosts文件

    - 文件最后追加一行，内容为

      ```bash

        部署datanode节点的宿主机ip datanode节点容器的id

      ```

    - 举例：
      - 宿主机ip：192.168.2.10

      - 容器id：123456

      - hosts追加内容为

      ```bash
        192.168.2.10 123456
      ```

    - 使hosts生效

    - window

      ```bash
          ipconfig /flushdns
      ```

    - centos

      ```bash
        /etc/init.d/network restart
      ```

  - 注意
  **容器不能rm或者down，否则需要重新配制hosts。restart、stop、start无影响**

- 部署在同一台服务器
