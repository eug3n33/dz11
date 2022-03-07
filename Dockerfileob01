FROM ubuntu:20.04
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt-get update
RUN apt install -y wget
RUN apt install -y docker.io
RUN apt-get install -y default-jdk
RUN apt install -y maven git
WORKDIR /tmp/
RUN apt-get clean