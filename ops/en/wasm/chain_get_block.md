# CLI/API: Chain

## get_block

Get block information.

### Usage example

```shell
## CLI
tcli get block 5
tcli get block 0000000592d0ac5f87ef02d564479330ed97002dbaae58f2c4affb22bd6fd00c

## API
curl https://t1.flon.network/v1/chain/get_info
curl  https://t1.flon.network/v1/chain/get_block -X POST -d '{"block_num_or_id":5}'
curl  https://t1.flon.network/v1/chain/get_block -X POST -d '{"block_num_or_id":0000000592d0ac5f87ef02d564479330ed97002dbaae58f2c4affb22bd6fd00c}'

```

### Result example
```json
{
  "timestamp": "2025-01-22T08:02:04.000",
  "producer": "flon",
  "confirmed": 0,
  "previous": "00000004889471ec6bda97cc8643f7a04cb0d089ab6bb4a642372889f0b268c0",
  "transaction_mroot": "0000000000000000000000000000000000000000000000000000000000000000",
  "action_mroot": "bb5b48fc565311eda9874af0d40143f928501d36573ca95c1f33c21499189941",
  "schedule_version": 0,
  "new_producers": null,
  "producer_signature": "SIG_K1_K6i8FRQqmLZvBnoCG6vMWqHuTSJncUdLcXSJ7xaGbFZaAmfSLvYSU2cTgT1gAL1dfCQvuDyAkr2xVGGQSR2a2DYkQXtyJ4",
  "transactions": [],
  "id": "0000000592d0ac5f87ef02d564479330ed97002dbaae58f2c4affb22bd6fd00c",
  "block_num": 5,
  "ref_block_prefix": 3573739399
}
```