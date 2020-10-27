# ES

## 5.4.2

## 7.8.0

## 注意修改宿主机的配置

    vim /etc/sysctl.conf
    # 新增内容
    vm.max_map_count=262144
    # 读取配置
    sysctl -p
    # 检查
    sysctl -a | grep 'vm.max_map_count'

## 宿主机内存至少2G内存

## 文件夹权限改成 777

    chmod -R 777 es路径

## 启动限制

    ES无法以root用户启动，需要新建一个用户
