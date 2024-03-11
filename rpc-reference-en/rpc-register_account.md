# register_account

The register_account command registers a local account as an on-chain account. Registering an account requires 5LIGO as a handling fee. This handling fee is obtained by the miners who package it.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "register_account",
  "params": ["test", "true"],
  "id": 1
}
```

> Input parameters

* Account name required to be registered
* Whether to broadcast to the chain (true / false)

>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": {
        "ref_block_num": 64907,
        "ref_block_prefix": 3421029415,
        "expiration": "2019-06-18T00:47:40",
        "operations": [
            [
                5,
                {
                    "fee": {
                        "amount": 500000,
                        "asset_id": "1.3.0"
                    },
                    "registrar": "1.2.0",
                    "referrer": "1.2.0",
                    "referrer_percent": 0,
                    "name": "test",
                    "owner": {
                        "weight_threshold": 1,
                        "account_auths": [],
                        "key_auths": [
                            [
                                "15PVU8X8fKXHNes7Q47PRj7txTJcVsZXgxQJD3KkGKUpkjbZu2h",
                                1
                            ]
                        ],
                        "address_auths": []
                    },
                    "active": {
                        "weight_threshold": 1,
                        "account_auths": [],
                        "key_auths": [
                            [
                                "15PVU8X8fKXHNes7Q47PRj7txTJcVsZXgxQJD3KkGKUpkjbZu2h",
                                1
                            ]
                        ],
                        "address_auths": []
                    },
                    "payer": "CNiRFXW8qpvfNGU4ewhKQEngiVHNTngxYyb",
                    "options": {
                        "memo_key": "15PVU8X8fKXHNes7Q47PRj7txTJcVsZXgxQJD3KkGKUpkjbZu2h",
                        "voting_account": "1.2.5",
                        "num_witness": 0,
                        "num_committee": 0,
                        "votes": [],
                        "miner_pledge_pay_back": 10,
                        "extensions": []
                    },
                    "extensions": {}
                }
            ]
        ],
        "extensions": [],
        "signatures": [
            "2015d98b93455cec7aeffdb41508a1f85a6a8d53f934d92c77ab446699c776cca27ae3cb309bdf387c42e9bfb3b57e244a5b36f86f7437502e0f1d6d0d222f73b 5"
        ],
        "block_num": 0,
        "trxid": "0b94f40bfb7c6fac5bb6a3ac23805d56791905f9"
    }
}
```

> return value

If successful, return to registration transaction.

- **expiration**: transaction expiration time
- **operations**: transaction operations
  - **5**: Indicates the registration account operation type
  - **fee**: handling fee
  - **name**: registered account name
  - **payer**: payer address
  - **max_supply**: maximum supply
- **signatures**: signatures
- **trxid**: transaction id
- **block_num**: Confirm block height, currently 0