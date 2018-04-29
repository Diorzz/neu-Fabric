# 组织结构与证书秘钥配置

想要搭建自己的`Fabric`网络，首先需要明确网络拓扑，确定有哪些节点和具体的节点类型。此外，`Fabric`通过证书和秘钥来管理节点的身份。因此，当确定网络拓后就需要为每个节点生成证书和秘钥。
> 在下文中我们指定`$FABRIC_ROOT`为`fabric`源码的根目录

## 说明
`Fabric`提供了一个方便的工具：`cryptogen`来生成这些配置文件。`cryptogen`工具在源码目录`./release/darwin-amd64/bin`或`./release/linux-amd64/bin`下。`cryptogen`工具会根据配置文件来生成相关证书和秘钥。默认配置文件名为`crypto-config.yaml`，我们可以在源码目录`./examples/e2e_cli/`下找到示例文件。在我们的当前目录`config`目录下存放了示例的配置文件，可以查看。

## 使用
当配置好配置文件`crypto-config.yaml`后就可以使用`crytogen`工具生成证书和密钥了，首先进入`$FABRCI_ROOT/release/inux-amd64/bin`目录下执行：
```shell
$ ./cryptogen generate --config <inpath> --output <outpath>
```

其中，`<inpath>`是`crypto-config.yaml`配置文件的路径，`<outpath>`是执行命令输出文件存放的路径。当命令执行成功后会在`<outpath>`目录下生成如下文件夹：
- ordererOrgnizations
- peerOrgnizations

这两个文件夹分别存放了各个节点的证书和密钥相关文件，在这里不详细介绍了。在我们后续的多节点环境部署下，我们需要用到这些文件。
