#RPC Introduction

[[toc]]

RPC is the basic interface for external applications to interact with the LIGO chain. The RPC service provided by LIGO chain complies with the JSONRPC 2.0 specification. External applications initiate RPC requests with the LIGO chain to obtain data on the chain and perform necessary operations on the LIGO chain. For example, create an account, register an account, cross-chain recharge, cross-chain withdrawal, transfer, call smart contract, voting and mining, etc. All LIGO chain functions can be called by external programs through the RPC interface.

> How to use RPC services

1. Please refer to [Start RPC service](/zh/dev/docking-exchange.html#How to start rpc server monitoring)
2. Please refer to [RPC specification](/zh/dev/docking-exchange.html#RPC usage specification)

> noun

1. `Smart contract id`: Each smart contract is represented by a unique hash value, which we call `smart contract id`, also known as `smart contract address`.

This chapter provides a complete reference manual for the RPC interface.