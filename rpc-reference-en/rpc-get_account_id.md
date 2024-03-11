# get_account_id

The get_account_id command gets the account id through the account name.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "get_account_id",
  "params": ["nathan"],
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
    "result": "1.2.38"
}
```

> return value

- **result**: ID corresponding to the account name