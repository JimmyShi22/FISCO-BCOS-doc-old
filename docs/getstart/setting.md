## 配置链

生成创世块

``` shell
sh generate_genesis.sh /mydata 
```

生成链证书

``` shell
sh generate_chain_cert.sh /mydata ca
```

## 配置机构

生成机构证书，假设机构名为WB

```shell
sh generate_agency_cert.sh /mydata /mydata/ca WB
```
## 配置节点

编写节点模板文件

``` shell
vim node_xxx.sample
```

生成节点

``` shell
sh generate_node.sh node_xxx.sample
```