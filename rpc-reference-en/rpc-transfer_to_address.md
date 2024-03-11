# transfer_to_address

The transfer_to_address command transfers assets to the specified address.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "transfer_to_address",
  "params": ["nathan","CNiRFXW8qpvfNGU4ewhKQEngiVHNTngxYyb","23","IGO","hello world",true],
  "id": 1
}
```

> Input parameters

* Transfer account name
* receiving address
* transfer amount
* Asset symbols (IGO, LIGO,BTC)
* Remarks, can be empty
* Whether to broadcast the transaction (true / false)

>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": {
        "ref_block_num": 52072,
        "ref_block_prefix": 1645038450,
        "expiration": "2019-06-17T07:07:20",
        "operations": [
            [
                0,
                {
                    "fee": {
                        "amount": 201,
                        "asset_id": "1.3.0"
                    },
                    "from": "1.2.0",
                    "to": "1.2.0",
                    "from_addr": "CNa5ZMhvFYXSYN4E2sAKqDVBKZgU9AGEBfZ",
                    "to_addr": "CNiRFXW8qpvfNGU4ewhKQEngiVHNTngxYyb",
                    "amount": {
                        "amount": 2300000,
                        "asset_id": "1.3.0"
                    },
                    "memo": {
                        "from": "mhsLQjB4NoJbMJBXzFcc4sSskdXpGbBDr2",
                        "to": "mhsLQjB4NoJbMJBXzFcc4sSskdXpGbBDr2",
                        "nonce": 0,
                        "message": "0000000068656c6c6f20776f726c64"
                    },
                    "extensions": []
                }
            ]
        ],
        "extensions": [],
        "signatures": [
            "2047cf318e4715b7a2f251eb53db4a1d9d608eca0d25207ea07600e3317f42a29b6c062247e86aef5917873132cacf3c5c2b3a66a06304df8a02d78617b27f4309 "
        ],
        "block_num": 0,
        "trxid": "78fdd4ed7c828d0f71d536c163b30e19dfd3d411"
    }
}
```

> return value

- **expiration**: transaction expiration time
- **operations**: list of transaction operations
  - **fee**: handling fee
  - **from_addr**: transfer-out address
  - **to_addr**: receiving address
  - **amount**: amount
  - **memo**: remarks
- **trxid**: transaction id
- **block_num**: Confirmation block, which is 0 at this time. If the package is successful, it can be found in the blockchain browser
- **signatures**: transaction signatures