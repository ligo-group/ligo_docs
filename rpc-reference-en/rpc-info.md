# info

The info command outputs some important information when the LIGO chain is running.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "info",
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
        "head_block_num": 3470221,
        "head_block_id": "0034f38dd587c9aefc18e3ab7f979c4a57085199",
        "head_block_age": "3 seconds old",
        "version": "1.2.20",
        "next_maintenance_time": "23 hours in the future",
        "chain_id": "2e13ba07b457f2e284dcfcbd3d4a3e4d78a6ed89a61006cdb7fdad6d67ef0b12",
        "participation": "92.96875000000000000",
        "round_participation": "88.00000000000000000",
        "scheduled_citizens": [
            "1.6.247",
            "1.6.270",
            "1.6.12",
            "1.6.1",
            "1.6.9",
            "1.6.246",
            "1.6.40",
            "1.6.16",
            "1.6.14",
            "1.6.15",
            "1.6.2",
            "1.6.113",
            "1.6.6",
            "1.6.80",
            "1.6.109",
            "1.6.271",
            "1.6.17",
            "1.6.7",
            "1.6.13",
            "1.6.24",
            "1.6.8",
            "1.6.10",
            "1.6.22",
            "1.6.21",
            "1.6.4"
        ]
    }
}
```

> Return parameters

- **head_block_num**: latest block height
- **head_block_id**: hash of the latest block
- **head_block_age**: The time since the latest block was generated
- **version**: ligo_client version number
- **next_maintenance_time**: ~~Not used yet~~
- **chain_id**: chain id, used to distinguish different chains (such as main chain and test chain)
- **participation**: Cumulative participation rate, the higher it is, the more stable the network is.
- **round_participation**: The participation rate of the current round is related to the progress of this round. The higher the rate, the more stable the miners participating in this round are. The lower rate may also mean that the progress of this round is relatively low. It needs to be combined with the number of miners participating in this round. judge
- **scheduled_citizens**: list of miners in the current round