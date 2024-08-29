# 使用一个基础的 Ubuntu 镜像
FROM ubuntu:20.04

# 安装必要的软件包
RUN apt-get update && apt-get install -y \
    wget \
    tar \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# 下载并安装 Go 1.13.6
RUN wget https://golang.org/dl/go1.13.6.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go1.13.6.linux-amd64.tar.gz && \
    rm go1.13.6.linux-amd64.tar.gz

# 设置 Go 环境变量
ENV PATH="/usr/local/go/bin:${PATH}"