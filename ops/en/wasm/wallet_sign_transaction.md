# API: Wallet

## sign_transaction
Given the signature transaction of a transaction array, the public key and Chain ID are required

### Usage example

```shell
## API
curl http://localhost:8889/v1/wallet/sign_transaction -X POST -d '[{"ref_block_num":21453,"ref_block_prefix":3165644999,"expiration":"2017-12-08T10:28:49","scope":["initb","initc"],"read_scope":[],"messages":[{"code":"currency","type":"transfer","authorization":[{"account":"initb","permission":"active"}],"data":"000000008093dd74000000000094dd74e803000000000000"}],"signatures":[]}, ["EOS6MRyAjQq8ud7hVNYcfnVPJqcVpscN5So8BhtHuGYqET5GDW5CV"], ""]'```

```

### Result example

```json
{
  "ref_block_num": 21453,
  "ref_block_prefix": 3165644999,
  "expiration": "2017-12-08T10:28:49",
  "scope": [
    "initb",
    "initc"
  ],
  "read_scope": [],
  "messages": [
    {
      "code": "currency",
      "type": "transfer",
      "authorization": [
        {
          "account": "initb",
          "permission": "active"
        }
      ],
      "data": "000000008093dd74000000000094dd74e803000000000000"
    }
  ],
  "signatures": [
    "1f393cc5ce6a6951fb53b11812345bcf14ffd978b07be386fd639eaf440bca7dca16b14833ec661ca0703d15e55a2a599a36d55ce78c4539433f6ce8bcee0158c3"
  ]
}
```