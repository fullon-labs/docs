# CLI/API: Chain

## get_info

Get the latest information related to the node.

### Usage example

```shell

## API
curl https://t1.flon.network/v1/chain/get_info

```

### Result example
```json
{
  "server_version": "825cffe9",
  "chain_id": "45a645b3a0de3e6f4860bfca3236550e6afb8b752f59c8954a54fa647583d406",
  "head_block_num": 8297924,
  "last_irreversible_block_num": 8297923,
  "last_irreversible_block_id": "007e9dc3f3ab1be3312dc83caafab3d8988d3f7ea8abfeed641f830496d3bd6f",
  "head_block_id": "007e9dc406d37f00b83151c963bd15bb14546bd72118765ce11954b310b0280a",
  "head_block_time": "2025-03-11T08:31:23.500",
  "head_block_producer": "flon",
  "virtual_block_cpu_limit": 200000000,
  "virtual_block_net_limit": 1048576000,
  "block_cpu_limit": 200000,
  "block_net_limit": 1048576,
  "server_version_string": "v1.0.2",
  "fork_db_head_block_num": 8297924,
  "fork_db_head_block_id": "007e9dc406d37f00b83151c963bd15bb14546bd72118765ce11954b310b0280a",
  "server_full_version_string": "v1.0.2-825cffe97aefc7f67de0ecba9fc538f0498e2cc3-dirty",
  "total_cpu_weight": 8761000,
  "total_net_weight": 8761000,
  "earliest_available_block_num": 1,
  "last_irreversible_block_time": "2025-03-11T08:31:23.000"
}
```

## get_block

Get block information.

### Usage example

```shell
## CLI

tcli get block 5
tcli get block 0000000592d0ac5f87ef02d564479330ed97002dbaae58f2c4affb22bd6fd00c

## API
curl  https://t1.flon.network/v1/chain/get_block -X POST -d '{"block_num_or_id":5}'

curl  https://t1.flon.network/v1/chain/get_block -X POST -d '{"block_num_or_id":"0000000592d0ac5f87ef02d564479330ed97002dbaae58f2c4affb22bd6fd00c"}'

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