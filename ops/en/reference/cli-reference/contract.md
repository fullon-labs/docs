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
tcli push action $contract_name $action_name $params -p $issuer

## Samples:
#   tcli  push action currencyview view '["userb"]' -p usera
#
```

# Read state data out of a contract

```
# enquire currency stats
tcli get currency stats $token_contract $symbol

# Samples:
#
#   tcli get currency stats flon.token FLON
#
```

# Get ABI info of a contract
```
tcli get abi $contract

# Samples:
#   `tcli get abi flon.xchain`
#
```

# Get data via primary index of a contract
```
tcli get table $code $scope $table $options

# Samples:
#    tcli get table flon.xchain flon.xchain global
#    tcli get table flon.xchain flon.xchain xinaddrmap
#    tcli get table flon.xchain flon.xchain coins -l 1 -r
#    tcli get table flon.xchain flon.xchain xinorders -l1
#    tcli get table flon.xchain flon.xchain xinorders -l1 -r
```

# Get data via secondary index of a contract

```
tcli get table $code $scope $table --index $indexNum --key-type $keyType $options

# Samples:
#    tcli get table amax.xchain amax.xchain xinorders --index 2 --key-type i64 -r -l1
#
```