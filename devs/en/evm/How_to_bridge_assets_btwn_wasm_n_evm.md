# How to move assets from `FLON EVM`to `FLON WASM` and vice versa

1. ## FLON WASM to FLON EVM

如果你在FullOn的测试网上有`FLON`测试代币, 那么你可以直接发送`FLON`到EVM合约地址(`flon.evm`), 同时把目标的EVM地址放到转账交易的`memo`字段。

举例如下：

```shell
./fucli --wallet-url=http://127.0.0.1:6666 --url=https://evmapi-t.flon.network transfer bobtestaccou flon.evm "100.0000 FLON" "0x5B38Da6a701c568545dCfcB03FcB875f56beddC4"
```

也可以从中心化交易所(例:币安)往`flon.evm`合约直接提取，但是要加上EVM地址作为相应的memo

2. ## 从FLON EVM到FLON

**FLON EVM跨链桥还在建设中**