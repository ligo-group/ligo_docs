# get_ntp_info

The get_ntp_info command outputs the current ntp information in the ligo_client and ligo_node programs.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "get_ntp_info",
  "params": [""],
  "id": 1
}
```
>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": [
        [
            "cli_wallet",
            {
                "_last_valid_ntp_reply_received_time": "2019-06-13T00:55:45",
                "_last_ntp_delta_initialized": true,
                "_last_ntp_delta_microseconds": -1608972
            }
        ],
        [
            "witness_node",
            {
                "_last_valid_ntp_reply_received_time": "2019-06-13T00:21:21",
                "_last_ntp_delta_initialized": true,
                "_last_ntp_delta_microseconds": -1595806
            }
        ]
    ]
}
```

> Return parameters

- **_last_valid_ntp_reply_received_time**: The time when the ntp response was last received
- **_last_ntp_delta_initialized**: Whether the ntp error has been corrected
- **_last_ntp_delta_microseconds**: error in microseconds