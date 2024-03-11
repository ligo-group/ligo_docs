# transfer_to_address

The transfer_to_address command transfers assets to the specified account. The transfer account can be a local account or an on-chain registered account. If it is a local account but not in a wallet, the transfer address cannot be found and the transfer will fail.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "transfer_to_account",
  "params": ["nathan","test","23","IGO","hello world",true],
  "id": 1
}
```

> Input parameters

* Transfer account name
* Receive account name
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
        "ref_block_num": 52149,
        "ref_block_prefix": 3772745964,
        "expiration": "2019-06-17T07:13:45",
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
            "2038dad36cc5cf74522255cc953c9d90253d8fcacbcd614e9028f79f62a73aadff72bd5b835eab4aa90370b0cd54694cfb25648b82c12282cb1b17f929d74b2cf7"
        ],
        "block_num": 0,
        "trxid": "8705b6dec10349488cb3ae629ce56fc381db2564"
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