# postgis

## 版本

    pgsql：13
    postgis:3.0

### 默认安装的插件

- postgis
- postgis_topology
- fuzzystrmatch
- postgis_tiger_geocoder

### 更新postgis

    docker exec postgis update-postgis.sh

### 最大连接数
 data/postgresql.conf的max_connections。已改成1000
