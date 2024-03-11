# invoke_contract

The invoke_contract command calls contract methods.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "invoke_contract",
  "params": ["test", 0.0001, 10000, "CCYttAT61esjuoqThW8rnhqc2VLmYNEhrsD", "getBonus", ""],
  "id": 1
}
```

> Input parameters

* Call account name
* The gas price, that is, the amount of LIGO spent for single-step execution, is at least 0.00001
* The maximum number of gas steps. If the actual number of execution steps is less than this limit, the actual fee will be charged. If it is greater than this limit, the call will fail.
* Contract address (id)
*Contract method name
*Contract parameters, if no parameters are passed, empty string is passed

>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": {
        "ref_block_num": 65533,
        "ref_block_prefix": 2423819965,
        "expiration": "2019-06-18T01:49:20",
        "operations": [
            [
                79,
                {
                    "fee": {
                        "amount": 1200,
                        "asset_id": "1.3.0"
                    },
                    "invoke_cost": 10000,
                    "gas_price": 10,
                    "caller_addr": "CNiRFXW8qpvfNGU4ewhKQEngiVHNTngxYyb",
                    "caller_pubkey": "0344d3bcc10ea31fd7db3dd15cb7d4983e079a3634f0810e7d04d659529d401590",
                    "contract_id": "CCYttAT61esjuoqThW8rnhqc2VLmYNEhrsD",
                    "contract_api": "getBonus",
                    "contract_arg": ""
                }
            ]
        ],
        "extensions": [],
        "signatures": [
            "2022ea9e0fd94746ed35ef1d9d8c6a256c605fa6c9ee88a804e4dfa0db9d9fc84215c56e806118d0b32ffe39138b25a2248054470dd4f6ca3f99193c34852c64cb"
        ],
        "block_num": 0,
        "trxid": "e3cf4222cc7dfd70136e57e5a7595d500473e1b9"
    }
}
```

> return value

- **expiration**: transaction expiration time
- **operations**: transaction operations
  - **79**: Indicates the operation type of calling contract method
  - **fee**: handling fee
  - **gas_price**: gas price
  - **caller_addr**: method caller address
  - **caller_pubkey**: method caller’s public key
  - **contract_id**: contract id
  - **contract_api**: calling method name
- **signatures**: transaction signatures
- **trxid**: transaction id