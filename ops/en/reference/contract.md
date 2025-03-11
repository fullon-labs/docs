# WASM Contract

## set contract 

deploy a new contract or update a new contract.

### Usage example 
```shell
# must create $con account in advance and make sure it has sufficent FLON for gas

tcli set contract $con ./build/contracts/$contract_dir -p ${con}@active
```

## invoke contract

Invoke an action of the target contract

### Usage example
```shell
tcli push action $contract_name $action_name $params -p $issuer

## Samples:
#
#   tcli  push action currencyview view '["userb"]' -p usera
#
```

## Read contract

Get the state data out of a smart contract

```shell
# enquire currency stats
tcli get currency stats $token_contract $symbol

# Samples:
#
#   tcli get currency stats flon.token FLON
#
```

## Get contract ABI

Get contract ABI info

### Usage example
```shell
tcli get abi $contract

# Samples:
#
#   tcli get abi flon.xchain
#
```
## Get contract data via primary index

Get data via primary index of a contract

### Usage example
```shell
## CLI
tcli get table $code $scope $table $options

# Samples:
#
#    tcli get table flon.xchain flon.xchain global
#    tcli get table flon.xchain flon.xchain xinaddrmap
#    tcli get table flon.xchain flon.xchain coins -l 1 -r
#    tcli get table flon.xchain flon.xchain xinorders -l1
#    tcli get table flon.xchain flon.xchain xinorders -l1 -r
```

## Get contract data via 2ndary index
Get data via secondary index of a contract

### Usage example
```shell
tcli get table $code $scope $table --index $indexNum --key-type $keyType $options

# Samples:
#
#    tcli get table flon.xchain flon.xchain xinorders --index 2 --key-type i64 -r -l1
#
```