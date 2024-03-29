# transfer_to_contract

The transfer_to_contract command transfers assets to the contract.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "transfer_to_contract",
  "params": ["test", "CCYttAT61esjuoqThW8rnhqc2VLmYNEhrsD", 10, "IGO", "", 0.00001, 10000, true],
  "id": 1
}
```

> Input parameters

* Transfer account name
* Contract address (id)
* transfer amount
* Asset symbols (IGO, LIGO,BTC)

>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": {
        "ref_block_num": 65457,
        "ref_block_prefix": 3876718435,
        "expiration": "2019-06-18T01:43:00",
        "operations": [
            [
                81,
                {
                    "fee": {
                        "amount": 300,
                        "asset_id": "1.3.0"
                    },
                    "invoke_cost": 10000,
                    "gas_price": 1,
                    "caller_addr": "CNiRFXW8qpvfNGU4ewhKQEngiVHNTngxYyb",
                    "caller_pubkey": "0344d3bcc10ea31fd7db3dd15cb7d4983e079a3634f0810e7d04d659529d401590",
                    "contract_id": "CCYttAT61esjuoqThW8rnhqc2VLmYNEhrsD",
                    "amount": {
                        "amount": 1000000,
                        "asset_id": "1.3.0"
                    },
                    "param": ""
                }
            ]
        ],
        "extensions": [],
        "signatures": [
            "1f55219ef8dbd19f7b9313a12bdb0f7add5b2c2d229a4c95ee51f42141a3c412de70b4e00a28d7ebd928d105ead7f0d97bb5b5076829df4e80abc5682ab9f6377e"
        ],
        "block_num": 0,
        "trxid": "e24eb80a85fd20c3e1fec770d9d4c59169e3e4f4"
    }
}
```

> return value

- **expiration**: transaction expiration time
- **operations**: transaction operations
  - **81**: Indicates the type of transfer operation to the contract
  - **fee**: handling fee
  - **gas_price**: gas price
  - **caller_addr**: method caller address
  - **caller_pubkey**: method caller’s public key
  - **amount**: transfer amount
  - **contract_id**: contract id
- **signatures**: transaction signatures
- **trxid**: transaction id