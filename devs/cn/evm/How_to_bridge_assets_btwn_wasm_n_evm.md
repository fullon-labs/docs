# 如何从`FLON EVM`账户资产跨链到`FLON WASM`账户和反向操作

1. ## 从FLON到FLON EVM

如果你在flon测试网上有FLON测试token, 那么你可以直接发送FLON到EVM地址。发送的时候只需要用EVM地址作为memo就可以。

举个例子

```shell
./focli --wallet-url=http://127.0.0.1:6666 --url=https://evmapi-t.flon.network transfer bobtestaccou flon.evm "100.0000 FLON" "0x5B38Da6a701c568545dCfcB03FcB875f56beddC4"
```

也可以从exchange往flon.evm合约直接提取，但是要加上EVM地址作为相应的memo

2. ## 从FLON EVM到FLON

**flon evm夸链桥还在建设中**