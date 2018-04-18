# Go install（Go语言环境安装）
***
`Fabric`是用`Go`语言开发的，并且其内部智能合约也是用`Go`语言写的，所以运行`fabric`需要`Go`语言环境。
## 下载Linux下`Go`的安装包
- 使用网址下载压缩包
> https://golang.org/doc/install?download=go1.10.1.linux-amd64.tar.gz

- 使用命令行下载（推荐）
> $ wget https://storage.googleapis.com/golang/go1.10.1.linux-amd64.tar.gz

## 解压压缩包到`/usr/local`目录下
> $ tar -C /usr/local -xzf go1.10.1.linux-amd64.tar.gz

## 设置`Go`的环境变量
- 设置`GOPATH`
> $ export GOPATH=/usr/local/go/

- 设置全局`PATH`
> $ export PATH=$PATH:$GOPATH/bin

- 设置`GOPATH`
> export GOPATH=$PATH:$GOROOT/bin

## 检查`Go`是否安装成功
> $ go version
