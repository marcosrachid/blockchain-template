# blockchain-template

Blockchain template with Ethereum

## Prerequisite

* [geth](https://geth.ethereum.org/downloads/)
* [NPM](https://nodejs.org/en/download/)

## Genesis.json

```
{
  "config": {
        "chainId": 15,
        "homesteadBlock": 0,
        "eip155Block": 0,
        "eip158Block": 0
    },
  "alloc"      : {}, // add ether to preallocated accounts
  "coinbase"   : "0x0000000000000000000000000000000000000000", // not required, defines where mining goes to when you have this account
  "difficulty" : "0x20000", // how difficult it is to mine a block
  "extraData"  : "",
  "gasLimit"   : "0x2fefd8", // upper limit to pay gas to miners on transactions
  "nonce"      : "0x0000000000000042", // initializing parameter for the blockchain
  "mixhash"    : "0x0000000000000000000000000000000000000000000000000000000000000000", // initializing parameter for the blockchain
  "parentHash" : "0x0000000000000000000000000000000000000000000000000000000000000000", // initializing parameter for the blockchain
  "timestamp"  : "0x00" // timestamp the block was generetad (Starting at 1970-01-01)
}
```

## Build

```
geth --datadir=./chaindata/ init ./genesis.json
```

## Execute

```
geth --datadir=./chaindata/
```
