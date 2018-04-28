# 组织结构与证书秘钥配置

想要搭建自己的`Fabric`网络，首先需要明确网络拓扑，确定有哪些节点和具体的节点类型。此外，`Fabric`通过证书和秘钥来管理节点的身份。因此，当确定网络拓后就需要为每个节点生成证书和秘钥。

`Fabric`提供了一个方便的工具：`cryptogen`来生成这些配置文件。`cryptogen`工具在源码目录`./release/darwin-amd64`或`./release/linux-amd64`下。`cryptogen`工具会根据配置文件来生成相关证书和秘钥。默认配置文件名为`crypto-config.yaml`，我们可以在源码目录`./examples/e2e_cli/`下找到示例文件。在我们的当前目录`config`目录下存放了示例的配置文件，可以查看。


