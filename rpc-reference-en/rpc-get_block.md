# get_block

The get_block command obtains block information by block height.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "get_block",
  "params": ["3537624"],
  "id": 1
}
```

> Input parameters

* The height of the block to be queried

>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": {
        "previous": "0035fad71b754a8ad3c00f2fb0756ab4ae111f2e",
        "timestamp": "2019-06-17T03:00:40",
        "trxfee": 361,
        "miner": "1.6.19",
        "transaction_merkle_root": "5a2906f23978581785a12fc86ca33d645460a473",
        "extensions": [],
        "next_secret_hash": "e276fa1c501f9be02b55e7953c6c102c938c14d7",
        "previous_secret": "768a8ed245b5cec132b1b9c2236a7e8c7562d944",
        "miner_signature": "1f77502c7de4b9eff92a9531c3c294acfb2b52bee0a3caac98a338dbbf05c2588330b25bd2117df832c3e31f2fde8a8cde2ea322be97e386f833840e1c1faa318 c",
        "transactions": [
            {
                "ref_block_num": 64211,
                "ref_block_prefix": 2123691888,
                "expiration": "2019-06-17T03:00:46",
                "operations": [
                    [
                        79,
                        {
                            "fee": {
                                "amount": 20100,
                                "asset_id": "1.3.0"
                            },
                            "invoke_cost": 2000000,
                            "gas_price": 1,
                            "caller_addr": "mhsLQjB4NoJbMJBXzFcc4sSskdXpGbBDr2",
                            "caller_pubkey": "02ad4f756a94fdc25aea170315a07b0c9e1f5e7472d8dc1cbb92712a03f86a92e2",
                            "contract_id": "CTpDxb8BTE1J1QDQeVfARG3sCkwBEAV76S",
                            "contract_api": "open",
                            "contract_arg": ""
                        }
                    ]
                ],
                "extensions": [],
                "signatures": [
                    "20630C3C1BF2E2670B829927087828835AEBE882406AF137FE8AEF253EEBB302864E5E3F0E88DB9246DC2D075BF917De07155D33 D83C "
                ],
                "operation_results": [
                    [
                        4,
                        {
                            "digest_str": "a0706036db297fc32c25f3fff48998f5695fd10b581b9deb7d9c90084a6585c9",
                            "api_result": "[\"{\\\"isOpen\\\":true,\\\"betOdds\\\":1.407000,\\\"betTime\\\":1560740430,\\\"betIndex \\\":2651,\\\"betPrice\\\":300000,\\\"betPlayer\\\":\\\"mhsLQjB4NoJbMJBXzFcc4sSskdXpGbBDr2\\\",\\\"betRandom\\\":68 ,\\\"betReward\\\":4.221000,\\\"betTarget\\\":71,\\\"currBlock\\\":3537622,\\\"betWinRatio\\\":70,\ \\"bankerReward\\\":0.064279}\",\"{\\\"isOpen\\\":true,\\\"betOdds\\\":1.492000,\\\"betTime\\\" :1560740430,\\\"betIndex\\\":2652,\\\"betPrice\\\":100000,\\\"betPlayer\\\":\\\"mhsLQjB4NoJbMJBXzFcc4sSskdXpGbBDr2\\\",\\\ "betRandom\\\":68,\\\"betReward\\\":0.000000,\\\"betTarget\\\":67,\\\"currBlock\\\":3537622,\\\"betWinRatio \\\":66,\\\"bankerReward\\\":0.000000}\"]",
                            "gas_count": 26001
                        }
                    ]
                ]
            }
        ],
        "number": 3537624,
        "block_id": "0035fad8df67a41ab982d5b269f163013ccb5717",
        "signing_key": "15PVU8X8fKXHNes7Q47PRj7txTJcVsZXgxQJD3KkGKUpkjbZu2h",
        "reward": 683861,
        "transaction_ids": [
            "f2a1720a4b1c17abbfa854768529887ed8fcb76a"
        ]
    }
}
```

> return value

Returns a collection of information voted for different Citizens, presented in an array. Each array element is an object, and its content means as follows:

- **previous**: previous hash
- **timestamp**: current block timestamp
- **miner**: block-producing miner id
- **transaction_merkle_root**: hash of transaction merkle root
- **previous_secret**: previous random number seed
- **miner_signature**: miner signature
- **transactions.expiration**: transaction expiration time
- **transactions.operations**: Transaction operations, the first field is the operation code, the second field is the operation object
- **number**: current block height
- **block_id**: current block hash
- **signing_key**: block reward
- **transaction_ids**: list of transaction ids contained in the block