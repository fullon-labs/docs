# Transaction

## transfer token

```shell
tcli transfer $from $to $quantity $memo
```

or 

```shell
tcli push action flon.token transfer '["$from","$to","$quantity","$memo"]' -p $from
```

## transfer via other token

```shell
tcli transfer -c flon.mtoken  $from $to $quantity $memo
```

or
```shell
tcli push action flon.mtoken transfer '["$from","$to","$quantity","$memo"]' -p $from
```

## create a new token

```shell
tcli push action $token_contract create '[ "$symbol", "$total_supply" ]' -p $token_contract@active
```
## issue new tokens

```shell
tcli push action $token_contract issue '[ "$symbol", "$total_supply", "" ]' -p $token_contract@active
```