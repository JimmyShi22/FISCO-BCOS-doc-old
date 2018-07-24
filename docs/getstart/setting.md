## 配置根证书

生成链的根证书

``` shell
#sh generate_chain_cert.sh -o 根证书生成的目录
sh generate_chain_cert.sh -o /mydata
```

## 配置机构

生成机构（agency）证书，假设机构名为agency0和agency1

```shell
#sh generate_agency_cert.sh -c 根证书所在目录 -o 机构证书生成目录 -n 机构名
sh generate_agency_cert.sh -c /mydata -o /mydata -n agency0
sh generate_agency_cert.sh -c /mydata -o /mydata -n agency1
```
## 配置节点

生成节点的目录、配置文件、启动脚本

``` shell
#sh generate_node -o 节点文件夹生成位置 -n 节点名 -l 节点监听的IP -r 节点的RPC端口 -p 节点的P2P端口 -c 节点的Channel Port端口 -e 节点Peers列表（可配置为：创世节点IP:创世节点P2P端口）
#创世节点
sh generate_node -o /mydata -n node0 -l 127.0.0.1 -r 8545 -p 30303 -c 8891 -e 127.0.0.1:30303
#其它节点
sh generate_node -o /mydata -n node1 -l 127.0.0.1 -r 8546 -p 30304 -c 8892 -e 127.0.0.1:30303
sh generate_node -o /mydata -n node2 -l 127.0.0.1 -r 8547 -p 30305 -c 8893 -e 127.0.0.1:30303
```

生成节点身份、证书

``` shell
#sh generate_node_cert.sh -a 机构名 -d 机构证书所在目录 -n 节点名 -o 节点文件夹的data目录
sh generate_node_cert.sh -a agency0 -d /mydata/agency0 -n node0 -o /mydata/node0/data
sh generate_node_cert.sh -a agency0 -d /mydata/agency0 -n node1 -o /mydata/node1/data
sh generate_node_cert.sh -a agency1 -d /mydata/agency1 -n node2 -o /mydata/node2/data
```
## 配置链

给每个节点生成创世块文件

``` shell
#sh generate_genesis.sh -d 创世节点 -o 创世块文件生成位置
sh generate_genesis.sh -d /mydata/node0 -o /mydata/node0
sh generate_genesis.sh -d /mydata/node0 -o /mydata/node1
sh generate_genesis.sh -d /mydata/node0 -o /mydata/node2
```
