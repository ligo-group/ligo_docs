# invoke_contract_offline

The invoke_contract_offline command calls the offline interface of the smart contract.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "invoke_contract_offline",
  "params": ["nathan", "mhsLQjB4NoJbMJBXzFcc4sSskdXpGbBDr2", "hello", "world"],
  "id": 1
}
```

> Input parameters

* Call account
*Contract address
*Method name
* Contract method parameters

>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": "hello world"
}
```

> return value

The return value is defined by each contract developer. Please refer to the specific contract interface documentation.