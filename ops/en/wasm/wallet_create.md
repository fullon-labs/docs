# API: Wallet

## wallet_create

Create a wallet with a given name.

### Usage example

```shell

## API
curl http://localhost:8889/v1/wallet/create -X POST -d '"default"'

```

### Result example

This command will return the password that can be used to unlock the wallet in the future.

```
PW5KFWYKqvt63d4iNvedfDEPVZL227D3RQ1zpVFzuUwhMAJmRAYyX
```