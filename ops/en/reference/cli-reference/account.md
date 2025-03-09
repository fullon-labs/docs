# Account

## get account info

```tcli get account $account_name```

## register an account

```shell
tcli system newaccount $creator --transfer $acct $pubkey \
    -p ${creator}@active
```

## get account balance

```shell
tcli get currency balance $token_contract $account $symbol
```