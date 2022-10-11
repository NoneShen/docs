# [MainNet](Zion_Setup.md) | [TestNet](Zion_Setup_TestNet.md) | DevNet

This is zion network setup configuration file ONLY in <strong>DEVNET</strong> mode, it's used to build and attach zion nodes.


## Git repo
https://github.com/polynetwork/zion/tree/master

## Genesis file
```dat
{
    "config": {
        "chainId": 60803, 
        "homesteadBlock": 0,
        "eip150Block": 0,
        "eip155Block": 0,
        "eip158Block": 0,
        "byzantiumBlock": 0,
        "constantinopleBlock": 0,
        "petersburgBlock": 0,
        "istanbulBlock": 0,
        "berlinBlock": 0,
        "londonBlock": 0,
        "hotstuff": {
            "protocol": "basic"
        }
    },
    "alloc": {
        "0x5Ed9a6713962f04DA057e6A949394e002855DF72": {"balance": "30000000000000000000000000"},
        "0xb06Bf71465eA8071e83a87f6b914f8FFA6829f4b": {"balance": "10000000000000000000000000"},
        "0x328C78eb1b265F380381879e8F332fbB622EBAe5": {"balance": "10000000000000000000000000"},
        "0xfEb056933BE960a183a0178249f7195AEbB74A4C": {"balance": "10000000000000000000000000"},
        "0x51d352512e592f7c50880a1fE280259fD68B07a2": {"balance": "10000000000000000000000000"},
        "0xF6AE2D66B8a30104360a0188A7E8Da98eb336075": {"balance": "10000000000000000000000000"},
        "0x347Da040f1079C40AA76A84DeD08028D3425CC9D": {"balance": "10000000000000000000000000"},
        "0x3d7ADdF663a30Ef02E086aE9eC37c311C892AFF5": {"balance": "10000000000000000000000000"}
    },
    "governance": [
        {"Validator": "0x258af48e28e4a6846e931ddff8e1cdf8579821e5", "Signer": "0x5Ed9a6713962f04DA057e6A949394e002855DF72"},
        {"Validator": "0x6a708455c8777630aac9d1e7702d13f7a865b27c", "Signer": "0xb06Bf71465eA8071e83a87f6b914f8FFA6829f4b"},
        {"Validator": "0x8c09d936a1b408d6e0afaa537ba4e06c4504a0ae", "Signer": "0x328C78eb1b265F380381879e8F332fbB622EBAe5"},
        {"Validator": "0xad3bf5ed640cc72f37bd21d64a65c3c756e9c88c", "Signer": "0xfEb056933BE960a183a0178249f7195AEbB74A4C"}
    ],
    "community_rate": 2000,
    "community_address": "0x79ad3ca3faa0F30f4A0A2839D2DaEb4Eb6B6820D",
    "coinbase": "0x0000000000000000000000000000000000000000",
    "difficulty": "0x1",
    "extraData": "0x0000000000000000000000000000000000000000000000000000000000000000f89d801ef85494258af48e28e4a6846e931ddff8e1cdf8579821e5946a708455c8777630aac9d1e7702d13f7a865b27c948c09d936a1b408d6e0afaa537ba4e06c4504a0ae94ad3bf5ed640cc72f37bd21d64a65c3c756e9c88cb8410000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c080",
    "gasLimit": "0x1fffff",
    "nonce": "0x4510809143055965",
    "mixhash": "0x0000000000000000000000000000000000000000000000000000000000000000",
    "parentHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
    "timestamp": "0x00"
}
```

## Contract address
```dat
        NodeManagerContractAddress       = common.HexToAddress("0x0000000000000000000000000000000000001000")
	EconomicContractAddress          = common.HexToAddress("0x0000000000000000000000000000000000001001")
	InfoSyncContractAddress          = common.HexToAddress("0x0000000000000000000000000000000000001002")
	CrossChainManagerContractAddress = common.HexToAddress("0x0000000000000000000000000000000000001003")
	SideChainManagerContractAddress  = common.HexToAddress("0x0000000000000000000000000000000000001004")
	RelayerManagerContractAddress    = common.HexToAddress("0x0000000000000000000000000000000000001005")
	Neo3StateManagerContractAddress  = common.HexToAddress("0x0000000000000000000000000000000000001006")
	SignatureManagerContractAddress  = common.HexToAddress("0x0000000000000000000000000000000000001007")
	ProposalManagerContractAddress   = common.HexToAddress("0x0000000000000000000000000000000000001008")
```

## Cross chain router
```dat
NO_PROOF_ROUTER    = uint64(0)
BTC_ROUTER         = uint64(1)
ETH_ROUTER         = uint64(2)
ONT_ROUTER         = uint64(3)
NEO_ROUTER         = uint64(4)
COSMOS_ROUTER      = uint64(5)
BSC_ROUTER         = uint64(6)
HECO_ROUTER        = uint64(7)
QUORUM_ROUTER      = uint64(8)
ZILLIQA_ROUTER     = uint64(9)
MSC_ROUTER         = uint64(10)
NEO3_LEGACY_ROUTER = uint64(11)
OKEX_ROUTER        = uint64(12)
NEO3_ROUTER        = uint64(14)
ETH_COMMON_ROUTER  = uint64(15)
```

## Machine
IP | SSH Port
---|---
101.32.99.70|32000
101.32.99.132|32000
124.156.214.163|32000
124.156.210.112|32000

## Nodes
Node Index | validator| signer| IP | Rpc Port | Ws Port | Mode
---|---|---|---|---|---|---
0|0x258af48e28E4A6846E931dDfF8e1Cdf8579821e5|0x5Ed9a6713962f04DA057e6A949394e002855DF72|101.32.99.70|22000|null|Miner
1|0x6A708455C8777630AaC9d1e7702d13F7a865b27C|0xb06Bf71465eA8071e83a87f6b914f8FFA6829f4b|101.32.99.70|22001|null|Miner
2|0x8c09D936a1B408D6e0afAA537ba4E06c4504a0AE|0x328C78eb1b265F380381879e8F332fbB622EBAe5|101.32.99.132|22000|null|Miner
3|0xAd3Bf5eD640CC72f37BD21d64A65C3C756e9C88C|0xfEb056933BE960a183a0178249f7195AEbB74A4C|101.32.99.132|22001|null|Miner
4|0xC095448424A5ECd5cA7CcDaDFaAD127a9d7E88ec|0x51d352512e592f7c50880a1fE280259fD68B07a2|124.156.214.163|22000|null|Backup Miner
5|0xD47a4e56e9262543Db39d9203CF1a2e53735f834|0xF6AE2D66B8a30104360a0188A7E8Da98eb336075|124.156.214.163|22001|null|Backup Miner
6|0xbfB558F0dceb07Fbb09E1C283048B551A4310921|0x347Da040f1079C40AA76A84DeD08028D3425CC9D|124.156.210.112|22000|null|Backup Miner
7|0x18468E8F088E470b04d540C67564cD48aD76Ee44|0x3d7ADdF663a30Ef02E086aE9eC37c311C892AFF5|124.156.210.112|22001|null|Backup Miner
8|null|null|124.156.210.112|22002|22003|Full archive

node8 support websocket services of `web3,eth`.