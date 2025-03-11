# CLI/API: Chain

## get_account

Get account information.

### Usage example

```shell
## CLI
tcli get account $account_name

## API
curl  https://t1.flon.network/v1/chain/get_account -X POST -d '{"account_name":"flon"}'
```