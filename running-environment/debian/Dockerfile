FROM debian:stable

LABEL "Author"="Teler" \
    "email"="teler96@qq.com" \
    version=0.0.1 \
    description="基础的开发环境"

RUN apt update -y && \
    apt install --no-install-recommends -y openjdk-11-jre \
                python3 \
                python3-pip && \
    pip3 install numpy openpyxl scikit-learn pandas && \
    ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ENV TZ=Asia/Shanghai
ENV LANG C.UTF-8