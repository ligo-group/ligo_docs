# is_locked

The is_locked command determines whether ligo_client is locked.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "is_locked",
  "params": [""],
  "id": 1
}
```
>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": false
}
```

> Return parameters

- **result**: true means locked, false means not locked