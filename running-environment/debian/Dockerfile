FROM debian

LABEL "Author"="Teler" \
    "email"="teler96@qq.com" \
    version=0.0.1 \
    description="基础的开发环境"

ENV TZ=Asia/Shanghai

RUN cp /dev/null /etc/apt/sources.list && \
    echo "deb http://mirrors.163.com/debian/ buster main non-free contrib" >>/etc/apt/sources.list && \
    echo "deb-src http://mirrors.163.com/debian/ buster main non-free contrib" >>/etc/apt/sources.list && \
    echo "deb http://mirrors.163.com/debian-security buster/updates main" >>/etc/apt/sources.list && \
    echo "deb-src http://mirrors.163.com/debian-security buster/updates main" >>/etc/apt/sources.list && \
    echo "deb http://mirrors.163.com/debian/ buster-updates main non-free contrib" >>/etc/apt/sources.list && \
    echo "deb-src http://mirrors.163.com/debian/ buster-updates main non-free contrib" >>/etc/apt/sources.list && \
    echo "deb http://mirrors.163.com/debian/ buster-backports main non-free contrib" >>/etc/apt/sources.list && \
    echo "deb-src http://mirrors.163.com/debian/ buster-backports main non-free contrib" >>/etc/apt/sources.list && \
    apt update -y && \
    apt install -y openjdk-11-jre \
                python3 \
                python3-pip && \
    pip3 install \
                scikit-learn \
                pandas \
                -i https://mirrors.aliyun.com/pypi/simple && \
    ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ENV LANG C.UTF-8