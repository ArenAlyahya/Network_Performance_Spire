FROM almalinux/9-base
#centos:centos8
#ubuntu:20.04 
#debian

#FROM centos:centos7
WORKDIR ./app


# Install dependencies
# not working
#RUN add-apt-repository ppa:ubuntuhandbook1/ppa
#RUN apt-get apt-utils
#RUN apt-get install libqt4-dev
#RUN apt-get install qt-sdk
#RUN apt-get qtbase5-dev

# worked
#RUN apt-get update
#RUN DEBIAN_FRONTEND=noninteractive  apt-get install qt5-default -y
#RUN apt-get install libssl-dev  -y
#RUN apt-get install flex byacc -y
#RUN apt-get install cmake -y


#RUN cd /etc/yum.repos.d/
#RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
#RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*


#RUN yum check-update

RUN yum clean all && yum update -y
RUN yum install openssl-devel -y

RUN yum install flex byacc -y

RUN yum install -y epel-release

RUN yum install -y qt5-qtbase-devel
RUN yum install -y qt5-qtwebkit-devel
RUN yum install -y qt5-qtsvg
RUN yum install -y qt5-qtsvg-devel
RUN yum install -y qt5-qttools-devel
RUN yum install -y qt5
RUN yum install -y qt5-qtmultimedia-devel
#RUN yum install -y qt5-*
RUN dnf --enablerepo=crb install -y qt5-devel
RUN yum install -y qt5* --skip-broken



RUN yum install cmake -y

RUN yum install -y autoconf
RUN yum install -y automake
RUN yum install -y bison


COPY . /app
RUN ls
RUN  cd spire
RUN pwd

RUN  make libs

EXPOSE 8120
EXPOSE 8100
EXPOSE 8900

EXPOSE 5053
EXPOSE 5052
EXPOSE 5051


