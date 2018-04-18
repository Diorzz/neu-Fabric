# Docker Install（Ubuntu下Docker安装）
***
本教程只针对`ubuntu`系统下的`Docker`安装，其他系统安装教程请访问`https://docs.docker.com/install/`。执行完本教程命令后您的电脑需要安装以下软件
- `docker`
- `docker-compose`

## 卸载旧版本
如果系统中已经安装过旧版本的`ubuntu`的系统，请先检查并卸载旧版本，命令代码如下：
 > $ sudo apt-get remove docker docker-engine docker.io

如果系统中没有安装过`Docker`则会提示`Package 'docker' is not installed, so not removed`那么你就可以执行下一步了。

## 配置Docker仓库（可选）
- 更新`apt`软件包
> $ sudo apt-get update

- 允许`apt`使用`HTTPS`安装包
> $ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
    
- 添加`Docker`官方 GPG 秘钥
> $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

- 确定你有如下指纹信息
> $ sudo apt-key fingerprint 0EBFCD88

输入上述命令后命令行会显示一些信息，确定查找是否有如下数据项：
> pub   4096R/0EBFCD88 2017-02-22
      Key fingerprint = 9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
uid                  Docker Release (CE deb) <docker@docker.com>
sub   4096R/F273FCD8 2017-02-22

- 创建仓库
> $ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

## 安装`docker`
- 更新`apt`包索引
> $ sudo apt-get update

- 安装`docker-ce`
> $ sudo apt-get install docker-ce

- 检查`Docker`是否安装成功
> $ docker --version

## 安装`docker-compose`
- 更新`apt`包索引
> $ sudo apt-get update

- 安装`docker-compose`
> $ sudo apt-get install docker-compose

- 检查`docker-compose`是否安装成功
> $ docker-compose --version
