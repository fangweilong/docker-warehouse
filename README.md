# docker-warehouse

## 介绍

    docker-compose构建文件

---

## 使用方法

### 进入文件夹

    cd /nginx

### 运行

    docker-compose up -d

### 停止

    docker-compose stop

### 重启

    docker-compose restart

### 删除

    docker-compose rm

### 校验配置文件

    docker-compose config  -q

---

## docker-compose.yml

    1.services下可以配置多个容器
    2.ports配置映射端口 可以多个
    3.volumes配置数据、conf等映射关系
