# get_asset_imp

The get_asset_imp command queries asset information by asset symbol.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "get_asset_imp",
  "params": ["IGO"],
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
    "result": {
        "id": "1.3.0",
        "symbol": "IGO",
        "precision": 5,
        "issuer": "1.2.3",
        "options": {
            "max_supply": "100000000000",
            "market_fee_percent": 0,
            "max_market_fee": "10000000000000000",
            "issuer_permissions": 0,
            "flags": 0,
            "core_exchange_rate": {
                "base": {
                    "amount": 1,
                    "asset_id": "1.3.0"
                },
                "quote": {
                    "amount": 1,
                    "asset_id": "1.3.0"
                }
            },
            "whitelist_authorities": [],
            "blacklist_authorities": [],
            "whitelist_markets": [],
            "blacklist_markets": [],
            "description": "",
            "extensions": []
        },
        "dynamic_asset_data_id": "2.3.0",
        "feeds": [],
        "publishers": [],
        "current_feed": {
            "settlement_price": {
                "base": {
                    "amount": 0,
                    "asset_id": "1.3.0"
                },
                "quote": {
                    "amount": 0,
                    "asset_id": "1.3.0"
                }
            },
            "maintenance_collateral_ratio": 1750,
            "maximum_short_squeeze_ratio": 1500,
            "core_exchange_rate": {
                "base": {
                    "amount": 0,
                    "asset_id": "1.3.0"
                },
                "quote": {
                    "amount": 0,
                    "asset_id": "1.3.0"
                }
            }
        },
        "current_feed_publication_time": "1970-01-01T00:00:00",
        "allow_withdraw_deposit": true,
        "dynamic_data": {
            "id": "2.3.0",
            "current_supply": "620005316300000",
            "confidential_supply": 0,
            "accumulated_fees": 0,
            "fee_pool": 0,
            "withdraw_limition": 0,
            "gas_price": "5000000000"
        }
    }
}
```

> return value

- **id**: asset id
- **symbol**: asset symbol
- **precision**: precision
- **issuer**: issuer
- **options**: asset options
  - **max_supply**: maximum supply
- **dynamic_data**: dynamic data
  - **current_supply**: current supply
  - **gas_price**: gas price