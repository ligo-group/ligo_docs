# network_get_info

The network_get_info command obtains local ligo_node runtime network information.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "network_get_info",
  "params": [""],
  "id": 1
}
```


>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": {
        "listening_on": "0.0.0.0:47517",
        "node_public_key": "033ab7ab451706f97416a4d7b75fafa94016326b964e16d1bbf8ff661dbc8fc5fa",
        "node_id": "479ddbfcb1dfd0522b837d645f7eb65e2c70c553d3605fb52c1b15aade330b1168",
        "firewalled": "unknown",
        "connections": 0,
        "current_block_height": 65713,
        "target_block_height": 65713,
        "connection_count": 0
    }
}
```

> return value

- **listening_on**: ligo_node listening port
- **node_public_key**: ligo_node public key
- **node_id**: ligo_node unique id
- **firewalled**: whether there is a firewall
- **connections**: number of links
- **current_block_height**: local block height
- **target_block_height**: target block height
- **connection_count**: number of links