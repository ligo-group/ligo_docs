#ntp_update_time

The ntp_update_time command updates the ntp time immediately. The update results can be viewed later via [get_ntp_info](/zh/dev/rpc-reference/rpc-get-ntp-info).

> Request
```
{
  "jsonrpc": "2.0",
  "method": "ntp_update_time",
  "params": [""],
  "id": 1
}
```
>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": null
}
```

> Return parameters

- **result**: returns null