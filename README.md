# svc-kujira-relay

IBC Paths created and maintained by Defiant Labs

## Wallets

- [kujira1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9ntcpas](https://www.mintscan.io/kujira/account/kujira1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9ntcpas)
- [akash1x9fxqdkg4rumkzrck8t3qnhm30jgfsx90ch7fq](https://www.mintscan.io/akash/account/akash1x9fxqdkg4rumkzrck8t3qnhm30jgfsx90ch7fq)
- [mantle1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9u8pu0s](https://www.mintscan.io/asset-mantle/account/mantle1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9u8pu0s)
- [cre1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9xtfu9h](https://www.mintscan.io/crescent/account/cre1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9xtfu9h)
- [omniflix1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9latq8y](https://www.mintscan.io/omniflix/account/omniflix1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9latq8y)
- [quasar1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9vqqyal](https://www.mintscan.io/quasar/account/quasar1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9vqqyal)
- [regen1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9ap39x7](https://www.mintscan.io/regen/account/regen1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9ap39x7)
- [somm1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9wl44ps](https://www.mintscan.io/sommelier/account/somm1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9wl44ps)

## Akash

[client Open](https://www.mintscan.io/akash/txs/4A550048A34E911103C7CF6ECDA6FE0A7A7CE1351555A6131618EB8CA8D150E8)  
[connection open](https://www.mintscan.io/akash/txs/A696C0CD664488BAAA8294D7443ED3209F5089390AE081480875820579C28BC2)  
[channel open](https://www.mintscan.io/akash/txs/80B902EC4207786A2E99A63A0F4E5FDCD81C067AA438BFAD2799038AED7829CB)

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: "defiantlabs"
  light-cache-size: 20
chains:
  akash:
    type: cosmos
    value:
      key: default
      chain-id: akashnet-2
      rpc-addr: https://akash-rpc.polkachu.com:443
      account-prefix: akash
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.025uakt
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
  kujira:
    type: cosmos
    value:
      key: default
      chain-id: kaiyo-1
      rpc-addr: https://kujira-rpc.polkachu.com:443
      account-prefix: kujira
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.025factory/kujira1qk00h5atutpsv900x202pxx42npjr9thg58dnqpa72f2p7m2luase444a7/uusk
      min-gas-amount: 0
      debug: true
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
paths:
  mainnet-kujira-akash:
    src:
      chain-id: kaiyo-1
      client-id: 07-tendermint-103
      connection-id: connection-72
    dst:
      chain-id: akashnet-2
      client-id: 07-tendermint-126
      connection-id: connection-103
    src-channel-filter:
      rule: "allowlist"
      channel-list: [channel-64]

```

## AssetMantle

[client Open](https://www.mintscan.io/asset-mantle/txs/1188EF1416F61AD60546F369FA6003D81D08703A769AB53F77600FFFAA0028A0)  
[connection open](https://www.mintscan.io/asset-mantle/txs/20FAB9CBD5241F88CC0B649440C91CEF7246997B325F5451F30598688B9AF4DA)  
[channel open](https://www.mintscan.io/asset-mantle/txs/D36FB0F9DFB69D8DBC08B3A99D614633E7AD4FD502BFEE4AB18EBFB800A7C2B5)

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: "defiantlabs"
  light-cache-size: 20
chains:
  assetmantle:
    type: cosmos
    value:
      key: default
      chain-id: mantle-1
      rpc-addr: https://rpc.assetmantle.one:443
      account-prefix: mantle
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.025umntl
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
  kujira:
    type: cosmos
    value:
      key: default
      chain-id: kaiyo-1
      rpc-addr: https://kujira-rpc.polkachu.com:443
      account-prefix: kujira
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.025factory/kujira1qk00h5atutpsv900x202pxx42npjr9thg58dnqpa72f2p7m2luase444a7/uusk
      min-gas-amount: 0
      debug: true
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
paths:
  mainnet-kujira-mantle:
    src:
      chain-id: kaiyo-1
      client-id: 07-tendermint-104
      connection-id: connection-73
    dst:
      chain-id: mantle-1
      client-id: 07-tendermint-50
      connection-id: connection-31
    src-channel-filter:
      rule: "allowlist"
      channel-list:
        - channel-65

```

## Crescent

[client Open](https://www.mintscan.io/crescent/txs/50DC70B24F301E2ADA25220B0BA110305A102326B975F8B48F46587C18635342)  
[connection open](https://www.mintscan.io/crescent/txs/860792C40141E0D42B6B54BFE451DC6104E9E2AE07ABA142ED32B136C60532E9)  
[channel open](https://www.mintscan.io/crescent/txs/35943EFE2AA2CAEF38838AA70B5BC51FD93755FCD1C3D66246017C3A23DA8EA5)

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: "defiantlabs"
  light-cache-size: 20
chains:
  crescent:
    type: cosmos
    value:
      key: default
      chain-id: crescent-1
      rpc-addr: https://crescent-rpc.polkachu.com:443
      account-prefix: cre
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.025ucre
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
  kujira:
    type: cosmos
    value:
      key: default
      chain-id: kaiyo-1
      rpc-addr: https://kujira-rpc.polkachu.com:443
      account-prefix: kujira
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.025factory/kujira1qk00h5atutpsv900x202pxx42npjr9thg58dnqpa72f2p7m2luase444a7/uusk
      min-gas-amount: 0
      debug: true
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
  mainnet-kujira-crescent:
    src:
      chain-id: kaiyo-1
      client-id: 07-tendermint-105
      connection-id: connection-75
    dst:
      chain-id: crescent-1
      client-id: 07-tendermint-78
      connection-id: connection-68
    src-channel-filter:
      rule: "allowlist"
      channel-list:
        - channel-67

```
## Omniflix

Waiting on account to exist on chain and funded.

[client Open]()  
[connection open]()  
[channel open]()

## Quasar

Waiting on account to exist on chain and funded.

[client Open]()  
[connection open]()  
[channel open]()

## Regen

Waiting on account to exist on chain and funded.

[client Open]()  
[connection open]()  
[channel open]()

## Sommelier

Waiting on account to exist on chain and funded.

[client Open]()  
[connection open]()  
[channel open]()