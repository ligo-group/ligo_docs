#get_account_lock_balance

The get_account_lock_balance command obtains voting information by account name.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "get_account_lock_balance",
  "params": ["abc"],
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
    "result": [
        {
            "id": "1.17.203932",
            "lockto_miner_account": "1.6.94",
            "lock_balance_account": "1.2.2088",
            "lock_balance_contract_addr": "InvalidAddress",
            "lock_asset_id": "1.3.0",
            "lock_asset_amount": "5000000000"
        },
        {
            "id": "1.17.203933",
            "lockto_miner_account": "1.6.45",
            "lock_balance_account": "1.2.2088",
            "lock_balance_contract_addr": "InvalidAddress",
            "lock_asset_id": "1.3.0",
            "lock_asset_amount": "9964800000"
        },
        {
            "id": "1.17.203934",
            "lockto_miner_account": "1.6.81",
            "lock_balance_account": "1.2.2088",
            "lock_balance_contract_addr": "InvalidAddress",
            "lock_asset_id": "1.3.3",
            "lock_asset_amount": "579998989000"
        }
    ]
}
```

> return value

Returns a collection of information voted for different Citizens, presented in an array. Each array element is an object, and its content means as follows:

- **id**: voting information id
- **lockto_miner_account**: The account id of the Citizen who received the vote
- **lock_balance_account**: voting account id
- **lock_balance_contract_addr**: voting contract address
- **lock_asset_id**: voting asset id
- **lock_asset_amount**: Amount of votes