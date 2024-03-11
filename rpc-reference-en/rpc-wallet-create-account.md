# wallet_create_account

The wallet_create_account command creates a local account and returns its address.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "wallet_create_account",
  "params": ["usdh"],
  "id": 1
}
```
> Input parameters

- The account name to be created. This account name is for local use. If you want to use this name permanently, you can call the registration account interface to register on the chain.

>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": "mhsLQjB4NoJbMJBXzFcc4sSskdXpGbBDr2"
}
```

> Return parameters

- **result**: LIGO address corresponding to the account