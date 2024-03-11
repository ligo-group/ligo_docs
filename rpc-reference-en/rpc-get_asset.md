# get_asset

The get_asset command obtains asset-related information on the LIGO chain.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "get_asset",
  "params": ["IGO"],
  "id": 1
}
```

> Input parameters

* The asset symbol to be queried

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
            "max_supply": "10000000000000000",
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
        "allow_withdraw_deposit": true
    }
}
```

> return value

- **id**: the id corresponding to the asset
- **symbol**: asset symbol
- **precision**: asset precision
- **issuer**: issuer account id
- **options.max_supply**: total supply
- **options.market_fee_percent**: ~~Not used yet~~
- **options.max_market_fee**: ~~Not used yet~~
- **options.issuer_permissions**: ~~Not used yet~~
- **options.flags**: ~~Not used yet~~
- **options.core_exchange_rate**: ~~Not used yet~~
- **options.whitelist_authorities**: ~~Not used yet~~
- **options.blacklist_authorities**: ~~Not used yet~~
- **options.whitelist_markets**: ~~Not used yet~~
- **options.blacklist_markets**: ~~Not used yet~~
- **options.description**: ~~Not used yet~~
- **options.extensions**: ~~Not used yet~~
- **dynamic_asset_data_id**: ~~Not used yet~~
- **feeds**: feed price transaction information
- **current_feed**: current price feed information
- **current_feed_publication_time**: current price feed time
- **allow_withdraw_deposit**: ~~Not used yet~~