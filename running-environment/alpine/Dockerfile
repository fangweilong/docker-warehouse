FROM python:3.7-alpine

LABEL "Author"="Teler" \
    "email"="teler96@qq.com" \
    version=0.0.1 \
    description="基础的开发环境"


RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories && \
    apk update && \
    apk add openjdk11-jre tzdata && \
    pip3 config set global.index-url https://mirrors.163.com/pypi/simple/ && \
    pip3 install openpyxl scikit-learn pandas && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone && \
    apk del tzdata && \
    rm -rf /tmp/* /var/cache/apk/* /root/.cache

WORKDIR /home/app