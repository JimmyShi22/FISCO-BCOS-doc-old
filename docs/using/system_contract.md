### 部署系统合约

**配置合约部署端口**

``` shell
vim .../web3lib/config.js
```

将``` proxy ```指向其中一个节点的RPC端口即可，合约部署时会自动同步给链上其它的节点。

``` javascript
var proxy="http://127.0.0.1:8545";
```

**部署系统合约**

``` shell
babel-node deploy.js 
```

部署成功，输出合约路由表

``` log
#.....省略很多编译warn信息.....
SystemProxycomplie success！
send transaction success: 0x56c9e34cf559b3a9aead8694a7bda7e6b5ea4af855d5ec6ef08fadf494accf08
SystemProxycontract address 0x210a7d467c3c43307f11eda35f387be456334fed
AuthorityFiltercomplie success！
send transaction success: 0x112b6ac9a61197920b6cbe1a71d8f8d4a6c0c11cd0ae3c1107d1626691bf1c35
AuthorityFiltercontract address 0x297e397a7534464a4e7448c224aae52f9614af77
Groupcomplie success！
send transaction success: 0x1be1fb1393e3a3f37f197188ea99de0a5dd1828cc9fc24638f678528f0e30c23
Groupcontract address 0xed0a1b82649bd22d947e5c3ca0b779aac8ee5edc
TransactionFilterChaincomplie success！
send transaction success: 0x704a614b10c5682c44a11e48305bad40a0809d1fc9e178ddec1218c52e7bc9d0
TransactionFilterChaincontract address 0x60d34569bc861b40a7552f89a198a89d8c99075e
CAActioncomplie success！
send transaction success: 0x75f890777b586060c3f94dc3396f5ad86c3e10f2eb9b8350bbc838beecf50ece
CAActioncontract address 0x6fbf3bef2f757c01e0c43fc1364207c1e8a19d08
NodeActioncomplie success！
send transaction success: 0x9d26304258608de5bf1c47ecb9b2ac79f5323e6b74cef7eddef1fb9893d5e98e
NodeActioncontract address 0xb5e0d2c6f1b9f40ea21fa8698a28d1662e8afa3e
send transaction success: 0x03c86b3dcd3d564a00a709b7cd6f1902cd4111cc30c71c62728deadc6e8d7511
ConfigActioncomplie success！
send transaction success: 0xa49205ff3ad697fda75019cb2bbf541a120c146b973f8c5d50b761fd5024b795
ConfigActioncontract address 0xb1e6d5f95c9cb39a9e4e3071b3765e08c30ea281
FileInfoManagercomplie success！
send transaction success: 0x10f8b3fa9efb129bb321cba26019f363aad1b1a162b9347f6638bf6d94de7c32
FileInfoManagercontract address 0x0c2422186429e81911b729fd25e3afa76231f9c7
FileServerManagercomplie success！
send transaction success: 0xd156ccb19fa9dc5313c124933a458b141a20cc2ce01334ce030940e9f907cb84
FileServerManagercontract address 0xb33485375d208a23e897144b6244e20d9c1e83d9
ConsensusControlMgrcomplie success！
send transaction success: 0xcfe0a0fc77910c127d31470e38707dfe70a7fb699abce3e9261ef55a4e50997c
ConsensusControlMgrcontract address 0x3414ef5c15848a07538a2fac57c09a549036b5e3
ContractAbiMgrcomplie success！
send transaction success: 0xc1e2c4e837edda0e215ca06aaa02eecb3a954acfafd498a049b7cf6cee410f5c
ContractAbiMgrcontract address 0xac919b98301804575bd2dc676330aa8f2637f7d5
#......省略若干行...........
send transaction success: 0x2a0f5f9eeb069fe61289e8c95cb4b6cf026859cd20e38e8e47c0788609d8aad1
send transaction success: 0xcd51375a90056e92a52869c63ec153f05722ab8ee56b5ae242b9114c4838e32b
send transaction success: 0x250c0fc5f34bfb73a6bc2a858b64287aa859f12651a3798d46d7269e7305bf6f
send transaction success: 0xff3aeddb55c9ac6868df0cde04466431c7286d93baa80e3826522a2a8ad9681a
send transaction success: 0x71d484aa4a90068e409a11800e9ae5df6143dd59e0cc21a06c1a0bbba4617307
send transaction success: 0x8bd093d44c99817685d21053ed468afa8f216bc12a1c3f5fe33e5cd2bfd045c0
send transaction success: 0x5b9acaab5252bf43b111d24c7ff3adac0121c58e59636f26dbe2ca71dd4af47d
send transaction success: 0x34fb9226604143bec959d65edb0fc4a4c5b1fe5ef6eead679648c7295099ac8b
send transaction success: 0xe9cac7507d94e8759fcc945e6225c873a422a78674a79b24712ad76757472018
register TransactionFilterChain.....
send transaction success: 0x814ef74b4123f416a0b602f25cc4d49e038826cf50a6c4fbc6a402b9a363a8d9
register ConfigAction.....
send transaction success: 0xdb4aaa57b01ca7b1547324bcbeeaaeaa591bf9962ea921d5ce8845b566460776
register NodeAction.....
send transaction success: 0x2c7f43c84e52e99178a92e6a63fb69b5dedf4993f7cbb62608c74b6256241b39
register CAAction.....
send transaction success: 0xcb792f508ca890296055a53c360d68c3c46f8bf801ce73818557e406cbd0618c
register ContractAbiMgr.....
send transaction success: 0xfdc0dd551eada0648919a4c9c5ffa182d042099d73fa802cf803bebf5068aec1
register ConsensusControlMgr.....
send transaction success: 0x7f6d95e6a49a1c1de257415545afb0ec7fdd5607c427006fe14a7750246b9d75
register FileInfoManager.....
send transaction success: 0xc5e16814085000043d28a6d814d6fa351db1cd34f7d950e5e794d28e4ff0da49
register FileServerManager.....
send transaction success: 0xbbbf66ab4acd7b5484dce365d927293b43b3904cd14063a7f60839941a0479a0
SystemProxy address :0x9fe9648f723bff29f940b8c18fedcc9c7ed2b91f
-----------------SystemProxy route ----------------------
get 0xb33485375d208a23e897144b6244e20d9c1e83d9
0 )TransactionFilterChain=>0x60d34569bc861b40a7552f89a198a89d8c99075e,false,250
1 )ConfigAction=>0xb1e6d5f95c9cb39a9e4e3071b3765e08c30ea281,false,251
2 )NodeAction=>0xb5e0d2c6f1b9f40ea21fa8698a28d1662e8afa3e,false,252
3 )CAAction=>0x6fbf3bef2f757c01e0c43fc1364207c1e8a19d08,false,253
4 )ContractAbiMgr=>0xac919b98301804575bd2dc676330aa8f2637f7d5,false,254
5 )ConsensusControlMgr=>0x3414ef5c15848a07538a2fac57c09a549036b5e3,false,255
6 )FileInfoManager=>0x0c2422186429e81911b729fd25e3afa76231f9c7,false,256
7 )FileServerManager=>0xb33485375d208a23e897144b6244e20d9c1e83d9,false,257
-----------------SystemProxy route ----------------------
```

上述输出内容中，重要的是系统代理合约地址，即SystemProxy合约地址。如：

```log
SystemProxycontract address 0x210a7d467c3c43307f11eda35f387be456334fed
```
将系统代理合约地址写入所有节点的配置文件

``` shell
vim node_xxx/config.json
```

重启所有节点，让系统合约生效

``` shell
cd node_xxx
sh stop.sh
sh start.sh
```

### 节点加入联盟

