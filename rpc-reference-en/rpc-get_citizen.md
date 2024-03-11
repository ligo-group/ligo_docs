# get_citizen

The get_citizen command obtains Citizen information by account name.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "get_citizen",
  "params": ["leo"],
  "id": 1
}
```

> Input parameters

* Account name to be queried

>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": {
        "id": "1.6.5",
        "miner_account": "1.2.10",
        "last_aslot": 3694158,
        "signing_key": "15PVU8X8fKXHNes7Q47PRj7txTJcVsZXgxQJD3KkGKUpkjbZu2h",
        "last_change_signing_key_block_num": 0,
        "vote_id": "1:4",
        "total_votes": 0,
        "url": "",
        "total_missed": 1447,
        "lockbalance_total": [
            [
                "BTC",
                {
                    "amount": "10530038999",
                    "asset_id": "1.3.1"
                }
            ],
            [
                "IGO",
                {
                    "amount": "128797361658",
                    "asset_id": "1.3.0"
                }
            ],
            [
                "LIGO",
                {
                    "amount": "86144232999",
                    "asset_id": "1.3.2"
                }
            ]
        ],
        "total_produced": 39636,
        "last_confirmed_block_num": 3538589,
        "pledge_weight": "551763069349",
        "pledge_rate": 0,
        "participation_rate": 100,
        "next_secret_hash": "74ade99b9428eb2b6dd6bbfd31462a07d4e1e95b"
    }
}
```

> return value

- **id**: Citizen id
- **miner_account**: account id
- **last_aslot**: The height of the most recently produced block
- **signing_key**: Signing public key
- **total_missed**: number of missed blocks
- **lockbalance_total**: pledged asset information
- **total_produced**: total number of produced blocks
- **last_confirmed_block_num**: height of the latest block produced
- **pledge_weight**: voting weight
- **next_secret_hash**: next random number seed