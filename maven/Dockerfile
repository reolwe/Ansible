FROM ubuntu:20.04
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt update
RUN apt install -y git
RUN apt install -y wget
#RUN apt install -y tomcat9
RUN apt install -y default-jdk
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN apt install -y maven
WORKDIR /boxfuse-sample-java-war-hello/
RUN ls -l
RUN mvn package
CMD ["mvn"]