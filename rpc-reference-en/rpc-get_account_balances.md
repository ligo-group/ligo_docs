#get_account_balances

get_account_balances queries the address based on the account name.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "get_account_balances",
  "params": ["zb"],
  "id": 1
}
```

> Input parameters

* account name

>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": [
        {
            "amount": 0,
            "asset_id": "1.3.0"
        }
    ]
}
```

> return value

Returns the user balance list, with multiple assets displayed separately. If there has never been a transfer to this address, the list is empty.

- **amount**: quantity
- **asset_id**: asset type id (can be viewed through get_asset)