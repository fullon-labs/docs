# CLI/API: Chain

## abi_bin_to_json

Serialize binary hex to json.

### Usage example

```shell

## API
curl  https://t1.flon.network/v1/chain/abi_json_to_bin -X POST -d '{"code":"currency", "action":"transfer", "args":{"from":"initb", "to":"initc", "quantity":1000}}'
```