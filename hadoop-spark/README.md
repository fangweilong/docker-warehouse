# 启动

```bash
  docker-compose up -d
```

# 外网无法访问

```bash
config/hdfs-site.xml 文件

<property><name>dfs.namenode.http-address</name><value>0.0.0.0:50070</value></property>

```
