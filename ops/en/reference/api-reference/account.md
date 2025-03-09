# Account

{% hint style="info" %}
**Good to know:** FullOn protocol supports abstract accounts that all other digital assets or on-chain permissions are associated with.
{% endhint %}

## get_account
Get account information

### get_account usage example
```shell
curl  https://t1.flon.network/v1/chain/get_account -X POST -d '{"account_name":"flon"}'
```

### get_account result example
```json
{
  "account_name": "flon",
  "head_block_num": 7987910,
  "head_block_time": "2025-03-09T13:27:56.500",
  "privileged": true,
  "last_code_update": "2025-01-22T08:04:36.000",
  "created": "2025-01-01T08:00:00.000",
  "core_liquid_balance": "799944595.7280 FLON",
  "ram_quota": -1,
  "net_weight": -1,
  "cpu_weight": -1,
  "net_limit": {
    "used": -1,
    "available": -1,
    "max": -1,
    "last_usage_update_time": "2025-03-09T13:27:56.500",
    "current_used": -1
  },
  "cpu_limit": {
    "used": -1,
    "available": -1,
    "max": -1,
    "last_usage_update_time": "2025-03-09T13:27:56.500",
    "current_used": -1
  },
  "ram_usage": 4207226,
  "permissions": [
    {
      "perm_name": "active",
      "parent": "owner",
      "required_auth": {
        "threshold": 1,
        "keys": [
          {
            "key": "FO5jNbZzDLuj6uKvtV8tMoAnECU3fMze89RYuVR5gWd7PLdKscp2",
            "weight": 1
          }
        ],
        "accounts": [],
        "waits": []
      },
      "linked_actions": []
    },
    {
      "perm_name": "owner",
      "parent": "",
      "required_auth": {
        "threshold": 1,
        "keys": [
          {
            "key": "FO5jNbZzDLuj6uKvtV8tMoAnECU3fMze89RYuVR5gWd7PLdKscp2",
            "weight": 1
          }
        ],
        "accounts": [],
        "waits": []
      },
      "linked_actions": []
    }
  ],
  "total_resources": null,
  "self_delegated_bandwidth": null,
  "refund_request": null,
  "voter_info": null,
  "rex_info": null,
  "subjective_cpu_bill_limit": {
    "used": 0,
    "available": 0,
    "max": 0,
    "last_usage_update_time": "2000-01-01T00:00:00.000",
    "current_used": 0
  },
  "eosio_any_linked_actions": []
}
```


## Creating users

{% openapi src="https://petstore3.swagger.io/api/v3/openapi.json" path="/user/createWithList" method="post" %}
[https://petstore3.swagger.io/api/v3/openapi.json](https://petstore3.swagger.io/api/v3/openapi.json)
{% endopenapi %}
