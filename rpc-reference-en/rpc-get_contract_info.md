#get_contract_info

The get_contract_info command obtains contract information on the chain based on the contract ID.

> Request
```
{
  "jsonrpc": "2.0",
  "method": "get_contract_info",
  "params": ["mhsLQjB4NoJbMJBXzFcc4sSskdXpGbBDr2"],
  "id": 1
}
```

> Input parameters

*Contract id to be queried

>Response

```
{
    "id": 1,
    "jsonrpc": "2.0",
    "result": {
        "id": "mhsLQjB4NoJbMJBXzFcc4sSskdXpGbBDr2",
        "owner_address": "CNa5ZMhvFYXSYN4E2sAKqDVBKZgU9AGEBfZ",
        "owner_name": "",
        "name": "",
        "description": "",
        "type_of_contract": "normal_contract",
        "registered_block": 372,
        "registered_trx": "854647f348b3de5194b990bc59b8d7c8a57553d0",
        "native_contract_key": "",
        "derived": [],
        "code_printable": {
            "abi": [
                "init"
            ],
            "offline_abi": [
                "hello"
            ],
            "events": [
                "hello"
            ],
            "printable_storage_properties": [],
            "printable_code": "1b476c7561100019930d0a1a0a0408040808785600000000000000000000028774001000000000000000000000205140000002c0000006c4000 0080000000a4808000ec8000008ac00080c7404001e24000001e000080cb0000008ac08080c7404001074140011c0100020d814002cac04002ecc000008ac08081a 600000126008000040000000405696e697404076c6f63616c7313010000000000000004068656c6c6f010000000100040000000001000000010000000100 0208000000224000001e4000804b00000000008000220000001ec0ff7f2600000126008000000000000000000000000000008000000010000000100000001000 0000100000001000000010000000100000001000000010000000670726f707300000000080000000000000000010000000100000001000208000000224000 001e4000804b00000000008000220000001ec0ff7f2600000126008000000000000000000000000000080000000100000001000000010000000100000001000 000010000000100000001000000010000000670726f707300000000080000000000000000070000000a000000010003040000004600400081400000644000 01260080000200000004067072696e740407b3f5cabcbbaf0100000000000000000040000000800000008000000080000000a000000010000000573656c6600 0000000400000001000000055f454e56000c0000000f0000000200050900000086004000c140000000018000a440800181800000c00080009dc00001a6000 00126008000030000000405656d6974040668656c6c6f040768656c6c6f2001000000000000000000090000000d0000000d0000000d0000000d0000000d0000000e00 00000e0000000e0000000e0000000f000000020000000573656c66000000000900000004617267000000000900000001000000055f454e561400000001000 0000100000005000000050000000a000000070000000c0000000c0000000c0000000c0000000c0000000c0000000c0000000c0000000c0000000c0000000f 0000000c00000026000000260000000300000009436f6e747261637401000000140000000853746f726167650200000014000000024d04000000140000000 1000000055f454e56",
            "code_hash": "a690f6b523fa951a51ca6fc2fe31d0f738fdd156"
        },
        "createtime": "2019-06-14T07:08:15"
    }
}
```

> return value

- **id**: contract id
- **owner_address**: the account address for registering the contract
- **owner_name**: the account name for registering the contract
- **name**: contract name
- **description**: contract description
- **type_of_contract**: contract type
- **registered_block**: The block number of the registered contract
- **registered_trx**: the transaction id of the registered contract
- **native_contract_key**: ~~Not used yet~~
- **derived**: ~~Not used yet~~
- **code_printable.abi**: contract abi
- **code_printable.offline_abi**: Contract offline abi
- **code_printable.events**: contract event
- **code_printable.printable_storage_properties**: ~~Not used yet~~
- **code_printable.printable_code**: hexadecimal contract bytecode
- **code_printable.code_hash**: code hash
- **createtime**: creation time