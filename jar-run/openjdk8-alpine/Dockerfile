FROM openjdk:8-alpine

LABEL "Author"="Teler" \
    "email"="teler96@qq.com" \
    version=0.0.1 \
    description="jar运行在docker中的示例系统"

COPY target/app.jar /home/app/app.jar
WORKDIR /home/app

ENTRYPOINT ["java","-jar","app.jar"]

EXPOSE 8080