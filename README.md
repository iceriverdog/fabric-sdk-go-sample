# BlockChain-IOT-demo
The demo code for BlockChain-IOT project
## Hyperledger Fabric Setup
**Golang**

	1. 下载安装包
		https://studygolang.com/dl/golang/go1.14.2.linux-amd64.tar.gz

	2. 解压到 /usr/local
		sudo tar -zvxf go1.14.2.linux-amd64.tar.gz -C /usr/local

	3. 配置环境变量
		sudo vi ~/.bashrc
		export GOROOT=/usr/local/go
		export GOPATH=$HOME/go
		export GOBIN=$GOPATH/bin
		export PATH=$GOPATH:$GOBIN:$GOROOT/bin:$PATH
		source ~/.bashrc

**Docker**

	1. 查看系统中是否已经安装Docker
		docker --version

	2. 使用如下命令安装 Docker 的最新版本(太慢，可以更换源#3)：
		sudo apt update
		sudo apt install docker.io

**Docker-compose**

	1. 确定系统中是否已安装docker－compose工具
		docker-compose --version

	2. 如系统提示未安装，则使用如下命令安装docker-compose工具
		sudo apt install docker-compose

		docker-compose --version
		
	3.启动 Docker
		sudo groupadd docker
		sudo gpasswd -a $USER docker
		newgrp docker
		docker ps
		sudo systemctl daemon-reload
		sudo systemctl restart docker
		
	4.测试, 返回 Hello from Docker!则成功！
		docker run hello-world

**dl 源码**

	1. HOME目录下创建路径,并进入该目录
		mkdir -p ~/go/src/github.com/hyperledger  && cd ~/go/src/github.com/hyperledger
		
	2. 下载 fabric 源码
		git clone https://github.com/hyperledger/fabric.git 

	3. 完成下载后， 切换fabric 版本
		git checkout -b 1.2 origin/release-1.2

	4. 编译二进制文件、镜像
		make release
		make docker

## Tea traceability

	[Tea traceability](https://github.com/iceriverdog/fabric-sdk-go-sample)


