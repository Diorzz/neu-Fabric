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
当你准备好上述依赖环境，就可以运行官网给出的测试`Fabric`环境了，这个环境叫做`Fabric Simple`，为了安装该环境，你需要执行以下步骤：

- 安装`curl`
> $ sudo apt-get install curl

- 下载文件

在你喜欢的目录下执行下面的命令：
> curl -sSL https://goo.gl/6wtTN5 | bash -s 1.1.0
