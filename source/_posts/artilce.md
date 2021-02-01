---
title: Docker 学习笔记
date: 2020-05-02 22:56:49
tags:
---
# docker 三要素
* 镜像（image）------------ 类比于类
* 容器（container）--------- 类比于对象
* 仓库（repository）------- 存放着镜像

# docker 相关命令使用
## 安装docker--ubuntu系统
````````````````~~```shell
sudo apt-get install docker-ce
```
## 镜像加速器文件配置
docker配置文件目录 /etc/docker/damemon.js
<pre><code>{
    "registry-mirrors": [
        "https://hub-mirror.c.163.com",
        "https://docker.mirrors.ustc.edu.cn",
        "https://mirror.ccs.tencentyun.com",
        "https://registry.docker-cn.com"
    ]
}</code></pre>
## 启动docker
<pre><code>sudo systemctl enable docker
sudo systemctl start docker
</code></pre>
## 添加当前用户组到docker用户组
<pre><code>sudo groupadd docker
sudo usermod -aG docker $USER
</code></pre>
