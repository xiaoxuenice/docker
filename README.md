#!/bin/sh
-------安装 docker----------------------------------------------------------
wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-18.03.1.ce-1.el7.centos.x86_64.rpm
yum localinstall docker-ce-18.03.1.ce-1.el7.centos.x86_64.rpm -y 
-------安装 docker----------------------------------------------------------
yum install -y yum-utils  device-mapper-persistent-data  lvm2
yum-config-manager --add-repo https://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo 
yum -y install docker-ce --nobest

