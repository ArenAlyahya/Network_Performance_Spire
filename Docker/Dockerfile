FROM ubuntu:20.04 
#debian

#FROM centos:centos7
WORKDIR ./app

COPY . /app

# Install dependencies
#RUN add-apt-repository ppa:ubuntuhandbook1/ppa
RUN apt-get update
#RUN apt-get apt-utils
#RUN apt-get install libqt4-dev
RUN DEBIAN_FRONTEND=noninteractive  apt-get install qt5-default -y
RUN apt-get install libssl-dev  -y
RUN apt-get install flex byacc -y
#RUN apt-get install qt-sdk
#RUN apt-get qtbase5-dev
RUN apt-get install cmake -y

RUN  cd ./spire

RUN  make libs

EXPOSE 8120
EXPOSE 8100
EXPOSE 8900

EXPOSE 5053
EXPOSE 5052
EXPOSE 5051

#RUN yum check-update

#RUN yum clean all && yum update
#RUN yum install openssl-devel

#RUN yum install flex byacc
#RUN yum install qt-devel epel-release qtwebkit-devel

