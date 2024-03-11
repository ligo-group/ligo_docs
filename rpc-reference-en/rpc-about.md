#about

The about command outputs the major libraries and version information used in program compilation. Mainly used for development and debugging.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "about",
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
        "client_version": "1.2.19-43-g0505034d",
        "graphene_revision": "0505034dea3f54ee4d09232b0d51461874c3547b",
        "graphene_revision_age": "14 days ago",
        "fc_revision": "0505034dea3f54ee4d09232b0d51461874c3547b",
        "fc_revision_age": "14 days ago",
        "compile_date": "compiled on May 29 2019 at 11:37:06",
        "boost_version": "1.64",
        "openssl_version": "OpenSSL 1.0.1g 7 Apr 2014",
        "build": "win32 64-bit"
    }
}
```

> Return parameters

- **client_version**: ligo_client version number
- **graphene_revision**: graphene library version number
- **graphene_revision_age**: The time since graphene library version was released
- **fc_revision**: fc library version number
- **fc_revision_age**: The time since the fc library version was released
- **compile_date**: Compilation date
- **boost_version**: boost library version number
- **openssl_version**: openssl library version number
- **build**: Compilation platform