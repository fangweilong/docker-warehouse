FROM alpine

LABEL "Author"="Teler" \
    "email"="teler96@qq.com" \
    version=0.0.1 \
    description="基础的开发环境"


RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories && \
    apk update && \
    apk add openjdk11-jre tzdata python3 py3-pip && \
    pip3 install scikit-learn pandas openpyxl -i https://mirrors.aliyun.com/pypi/simple && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone && \
    apk del tzdata && \
    rm -rf /tmp/* /var/cache/apk/* /root/.cache

WORKDIR /home/app