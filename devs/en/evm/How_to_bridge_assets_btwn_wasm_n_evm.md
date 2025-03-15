# How to move assets from `FullOn EVM`to `FullOn WASM` and vice versa

1. ## Send tokens from FullOn WASM to FullOn EVM

You can transfer your `FLON` token directly to the global EVM contract(`flon.evm`) with the memo filed filled with the target EVM address.

The command line example:

```shell
./focli --wallet-url=http://127.0.0.1:6666 --url=https://evmapi-t.flon.network transfer bobtestaccou flon.evm "100.0000 FLON" "0x5B38Da6a701c568545dCfcB03FcB875f56beddC4"
```

You can also withdraw FLON tokens from a CEX (E.g. Binance) by filling the to account as `flon.evm` and memo field with the EVM target address.

2. ## Send tokens from FullOn EVM to FullOn WASM

**FullOn EVM bridge under construction**