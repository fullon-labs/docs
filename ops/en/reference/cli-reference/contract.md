# WASM Contract

## deploy a new contract
```
# must create $con account in advance and make sure it has sufficent FLON for gas

tcli set contract $con ./build/contracts/$contract_dir -p ${con}@active
```

## update an existing contract

same as deploy

## call an action of the target contract

```
# E.g. tcli  push action currencyview view '["userb"]' -p usera

tcli push action $contract_name $action_name $params -p $issuer
```
