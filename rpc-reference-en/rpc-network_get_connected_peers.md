# network_get_connected_peers

The network_get_connected_peers command outputs information about other nodes that the current ligo_node is connected to.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "network_get_connected_peers",
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
        {
            "version": 0,
            "host": "117.78.44.37:9034",
            "info": {
                "addr": "117.78.44.37:9034",
                "addrlocal": "192.168.1.155:54766",
                "services": "00000001",
                "lastsend": 1560395365,
                "lastrecv": 1560395362,
                "bytessent": 61584,
                "bytesrecv": 42176,
                "conntime": "2019-06-13T02:55:03",
                "pingtime": "",
                "pingwait": "",
                "version": "",
                "subver": "BlockLinks Reference Implementation",
                "inbound": false,
                "firewall_status": "not_firewalled",
                "startingheight": "",
                "banscore": "",
                "syncnode": "",
                "fc_git_revision_sha": "0505034dea3f54ee4d09232b0d51461874c3547b (same as ours)",
                "fc_git_revision_unix_timestamp": "2019-05-29T03:29:14",
                "fc_git_revision_age": "15 days ago (same as ours)",
                "platform": "linux",
                "current_head_block": "0034f8d719c9968996a4680060be5483b16344fb",
                "current_head_block_number": 3471575,
                "current_head_block_time": "2019-06-13T03:09:05"
            }
        },
        {
            "version": 0,
            "host": "118.25.97.92:62871",
            "info": {
                "addr": "118.25.97.92:62871",
                "addrlocal": "192.168.1.155:54766",
                "services": "00000001",
                "lastsend": 1560395365,
                "lastrecv": 1560395355,
                "bytessent": 6528,
                "bytesrecv": 10480,
                "conntime": "2019-06-13T03:02:23",
                "pingtime": "",
                "pingwait": "",
                "version": "",
                "subver": "BlockLinks Reference Implementation",
                "inbound": false,
                "firewall_status": "not_firewalled",
                "startingheight": "",
                "banscore": "",
                "syncnode": "",
                "fc_git_revision_sha": "0505034dea3f54ee4d09232b0d51461874c3547b (same as ours)",
                "fc_git_revision_unix_timestamp": "2019-05-29T03:29:14",
                "fc_git_revision_age": "15 days ago (same as ours)",
                "platform": "win32",
                "current_head_block": "0034f8d719c9968996a4680060be5483b16344fb",
                "current_head_block_number": 3471575,
                "current_head_block_time": "2019-06-13T03:09:05"
            }
        }
    ]
}
```

> Return parameters

- **version**: ~~Not used yet~~
- **host**: Peer IP and port information
- **info.addr**: Peer IP and port information
- **info.addrlocal**: local IP and port information
- **info.services**: ~~Not used yet~~
- **info.lastsend**: last sent timestamp
- **info.lastrecv**: last received timestamp
- **info.bytessent**: Number of bytes sent
- **info.bytesrecv**: Number of bytes received
- **info.conntime**: connection time
- **info.pingtime**: ~~Not used yet~~
- **info.pingwait**: ~~Not used yet~~
- **info.version**: ~~Not used yet~~
- **info.subver**: ~~Not used yet~~
- **info.inbound**: Number of bytes received
- **info.firewall_status**: peer firewall status
- **info.startingheight**: ~~Not used yet~~
- **info.banscore**: ~~Not used yet~~
- **info.syncnode**: ~~Not used yet~~
- **info.fc_git_revision_sha**: fc library version hash
- **info.fc_git_revision_unix_timestamp**: fc library build time
- **info.fc_git_revision_age**: The time since the fc library was built
- **info.platform**: peer platform
- **info.current_head_block**: The latest block hash of the peer
- **info.current_head_block_number**: The latest block height of the peer
- **info.current_head_block_time**: The latest block time of the peer