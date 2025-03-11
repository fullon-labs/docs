# CLI/API: Chain

## get_table_rows

Get smart contract data.

### Usage example

```shell

## API
curl https://t1.flon.network/v1/chain/get_table_rows -X POST -d '{"scope":"inita", "code":"currency", "table":"account", "json": true}'

curl https://t1.flon.network/v1/chain/get_table_rows -X POST -d '{"scope":"inita", "code":"currency", "table":"account", "json": true, "lower_bound":0, "upper_bound":-1, "limit":10}'

```

### Result example
```json
{
  "rows": [
    {
      "account": "account",
      "balance": 1000
    }
  ],
  "more": false
}
```