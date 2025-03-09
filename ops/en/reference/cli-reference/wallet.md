# Wallet

## create a new wallet

```tcli create wallet -n $wallet_name```

## load a wallet

```tcli open wallet -n $wallet_name```

## unlock a wallet

```tcli wallet unlock -n $wallet_name --password $password```

## list wallets

```tcli wallet list```

## list all wallet keys

```tcli wallet keys```

## list wallet public and private keys

```tcli wallet private_keys -n test --password $password```

## create public & private key

```tcli  create key --to-console```

## import private key

```tcli wallet import -n $wallet_name --private-key $priv_key```