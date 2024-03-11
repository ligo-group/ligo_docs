#get_account_addr

get_account_addr queries the address based on the account name.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "get_account_addr",
  "params": ["x"],
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
    "result": "mhsLQjB4NoJbMJBXzFcc4sSskdXpGbBDr2"
}
```

> return value

- **result**: the address corresponding to the account name