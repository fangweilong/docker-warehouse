# 将jar部署到docker中的Dockerfile

## docker build

- 当前根目录
```bash
    docker build -t <name>:<version> .
```

- or 指定目录
```bash
    docker build -f <path>/Dockerfile -t <name>:<version> .
```

***

## docker-compose

在build基础上，运行
~~~ bash
    docker-compose up -d
~~~
