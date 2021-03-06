# Fabric 安装环境搭建
***
## 准备
若要运行`Fabric`网络，需要安装以下依赖
- `ubuntu`系统
- `docker`
- `go`
- `node.js`
- `python`

对于以上包的安装方法，在当前目录下`xx-install.md`文件下有详细说明

## 测试网络
当你准备好上述依赖环境，就可以下载`Fabric`的源代码了：
- 获取源码

新建任意一个目录，进入目录中执行以下命令后会在该目录下下载最新版的`Fabric`源代码，时间有点慢，需要耐心等待。下载成功后源文件被放在`/usr/local/sbin/src/github.com/hyperledger/fabric`目录中
> $ go get github.com/hyperledger/fabric


- 执行脚本命令

在`scripts/`目录下有一个`bootstrap.sh`的启动文件，他会为你自动下载所有`Fabric`需要的`docker`镜像，下载需要时间，请耐心等待。
> $ ./bootstrap.sh

- 启动测试网络

在源码目录下`/example/e2e_cil`中启动脚本
> bash network_setup.sh up

当你成功启动并且出现以下界面时，证明你的环境安装成功了：
