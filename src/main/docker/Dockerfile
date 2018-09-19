FROM java:8
# 指定作者
MAINTAINER luoyadongit@163.com
#指定存储点
VOLUME /tmp
#添加jar包
ADD target/eureka-server-docker-0.0.1-SNAPSHOT.jar /app.jar
RUN bash -c 'touch /app.jar' 
EXPOSE 1000
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
#构建镜像：docker build -t luoyadongit/eureka-server-docker:0.0.1 .  仓库名/镜像名:标签 Dockerfile相对路径
#运行镜像：docker run -d -p 1000:1000 eureka-server-docker:0.0.1 
#向公共Registry(Docker Hub)推送镜像:docker push luoyadongit/eureka-server-docker:0.0.1
#向私有库推镜像：docker push localhost:5000/luoyadongit/eureka-server-docker:0.0.1
#修改镜像标签：docker tag luoyadongit/eureka-server-docker:0.0.1 localhost:5000/luoyadongit/eureka-server-docker:0.0.1
#搭建私有仓库：docker run -d -p 5000:5000 --restart=always --name registry2 registry:2 



