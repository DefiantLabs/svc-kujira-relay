# svc-kujira-relay

IBC Paths created and maintained by Defiant Labs. If you want to participate in these paths feel free to use the CONFIGs below.

## FIN pair Proposals

Defiant Labs has created several proposals for adding new pairs to Kujira FIN.

- [akash](https://blue.kujira.app/govern/369)
- [assetmantle](https://blue.kujira.app/govern/370)
- [crescent](https://blue.kujira.app/govern/371)
- [neutron-coming-soon](https://blue.kujira.app/govern)
- [omniflixhub](https://blue.kujira.app/govern/372)
- [regen](https://blue.kujira.app/govern/374)
- [sommerlier](https://blue.kujira.app/govern/375)

## Wallets

- [kujira1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9ntcpas](https://www.mintscan.io/kujira/account/kujira1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9ntcpas)
- [akash1x9fxqdkg4rumkzrck8t3qnhm30jgfsx90ch7fq](https://www.mintscan.io/akash/account/akash1x9fxqdkg4rumkzrck8t3qnhm30jgfsx90ch7fq)
- [mantle1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9u8pu0s](https://www.mintscan.io/asset-mantle/account/mantle1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9u8pu0s)
- [cre1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9xtfu9h](https://www.mintscan.io/crescent/account/cre1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9xtfu9h)
- [neutron1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9xunm2a](https://www.mintscan.io/omniflix/account/neutron1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9xunm2a)
- [noble1x9fxqdkg4rumkzrck8t3qnhm30jgfsx92q03g5](https://www.mintscan.io/noble/account/noble1x9fxqdkg4rumkzrck8t3qnhm30jgfsx92q03g5)
- [omniflix1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9latq8y](https://www.mintscan.io/omniflix/account/omniflix1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9latq8y)
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
      debug: false
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
      debug: false
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
      rpc-addr: https://mainnet.crescent.network:26657
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
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
paths:
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

## Kava

[client Open](https://www.mintscan.io/kujira/txs/9472E10CCECD88728972A490317AA003482ED4C247A1E03B8A18A53C311996BE?height=11846227)  
[connection open](https://www.mintscan.io/kujira/txs/82CCEB3EBF24C5F4880E3BFA0B759E1287326E96F1A0843E1D76502219AEBACC?height=11846246)  
[channel open](https://www.mintscan.io/kujira/txs/482289DB65749D81B7D46CE7E4365071FC3284D7EC7F4C4C1337C36F76B8B60A?height=11846265)

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: ""
  light-cache-size: 20
chains:
  kava:
    type: cosmos
    value:
      key: default
      chain-id: kava_2222-10
      rpc-addr: https://kava-rpc.ibs.team:443
      account-prefix: kava
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.01ukava
      min-gas-amount: 0
      max-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 459
      signing-algorithm: ""
      broadcast-mode: batch
      min-loop-duration: 0s
  kujira:
    type: cosmos
    value:
      key: default
      chain-id: kaiyo-1
      rpc-addr: https://kujira-rpc.nodes.defiantlabs.net:443
      account-prefix: kujira
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.01ukuji
      min-gas-amount: 0
      max-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      signing-algorithm: ""
      broadcast-mode: batch
      min-loop-duration: 0s
paths:
  mainnet-kujira-kava:
    src:
      chain-id: kava_2222-10
      client-id: 07-tendermint-119
      connection-id: connection-156
      # Transfer channel
      # channel-id: channel-95
    dst:
      chain-id: kaiyo-1
      client-id: 07-tendermint-140
      connection-id: connection-106
      # Transfer channel
      # channel-id: channel-116
    src-channel-filter:
      rule: ""
      channel-list: []

```

## Neutron

[client Open](https://www.mintscan.io/kujira/txs/30ABB1B3FD2F027B6CD407F1A11A6CB163A677BB48E3BEBA7BB912DC9489D268?height=10713076)  
[connection open](https://www.mintscan.io/kujira/txs/30ABB1B3FD2F027B6CD407F1A11A6CB163A677BB48E3BEBA7BB912DC9489D268?height=10713076)  
[channel open](https://www.mintscan.io/kujira/txs/B53F1C710A688B4ED2A68FB5D1CB561BDF7DE6BAFD9596B6358E38E66B819244?height=10713362)

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: "defiantlabs"
  light-cache-size: 20
chains:
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
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
  neutron:
    type: cosmos
    value:
      key: default
      chain-id: neutron-1
      rpc-addr: https://neutron-rpc.polkachu.com:443
      account-prefix: neutron
      keyring-backend: test
      gas-adjustment: 1.3
      gas-prices: 0.05ibc/C4CFF46FD6DE35CA4CF4CE031E643C8FDC9BA4B99AE598E9B0ED98FE3A2319F9
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
paths:
  mainnet-kujira-neutron:
    src:
      chain-id: kaiyo-1
      client-id: 07-tendermint-112
      connection-id: connection-82
    dst:
      chain-id: neutron-1
      client-id: 07-tendermint-2
      connection-id: connection-2
    src-channel-filter:
      rule: "allowlist"
      channel-list:
        - channel-75
```

## noble

not created by defiant, just relayed.

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: "defiantlabs"
  light-cache-size: 20
chains:
  noble:
    type: cosmos
    value:
      key: default
      chain-id: noble-1
      rpc-addr: https://rpc.mainnet.noble.strange.love:443
      account-prefix: noble
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.0251ibc/EF48E6B1A1A19F47ECAEA62F5670C37C0580E86A9E88498B7E393EB6F49F33C0
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
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
paths:
  mainnet-kujira-noble:
    src:
      chain-id: kaiyo-1
      client-id: 07-tendermint-95
      connection-id: connection-65
    dst:
      chain-id: noble-1
      client-id: 07-tendermint-2
      connection-id: connection-4
    src-channel-filter:
      rule: "allowlist"
      channel-list: [channel-62]
```

## Omniflix

[client Open](https://www.mintscan.io/omniflix/txs/46A1E46E5C66B83CED3D53161F372875C8981C319C703D495E0306034B17B15E)  
[connection open](https://www.mintscan.io/omniflix/txs/24C61160794FF60FD368367B54B04C6536E8C34238C825A2A73AFFE6C5584AD9)  
[channel open](https://www.mintscan.io/omniflix/txs/82093478D66CF39A4CA32DD859E645525CE98360B771D7E847F9A3F4C6571752)

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: "defiantlabs"
  light-cache-size: 20
chains:
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
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
  omniflixhub:
    type: cosmos
    value:
      key: default
      chain-id: omniflixhub-1
      rpc-addr: https://rpc-omniflixhub-ia.cosmosia.notional.ventures:443
      account-prefix: omniflix
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.025uflix
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
paths:
  mainnet-kujira-omniflixhub:
    src:
      chain-id: kaiyo-1
      client-id: 07-tendermint-108
      connection-id: connection-78
    dst:
      chain-id: omniflixhub-1
      client-id: 07-tendermint-43
      connection-id: connection-36
    src-channel-filter:
      rule: "allowlist"
      channel-list:
        - channel-70
```

## Regen

[client Open](https://www.mintscan.io/regen/txs/2224F4E0BC2804A3F40737B8E49A98C61655F27D87787B851053835D1CF7B4C6)  
[connection open](https://www.mintscan.io/regen/txs/7E1E0F8EF60020D11678EBAB7610722740A276B8E42F29782F441E2665DB5616)  
[channel open](https://www.mintscan.io/regen/txs/E101A8E35CF06185F0FD7BA59B3C134BF5B826AB9E429E92DF847C094FBDC0C1)

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: "defiantlabs"
  light-cache-size: 20
chains:
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
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
  regen:
    type: cosmos
    value:
      key: default
      chain-id: regen-1
      rpc-addr: https://rpc-regen.ecostake.com:443
      account-prefix: regen
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.025uregen
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
paths:
  mainnet-kujira-regen:
    src:
      chain-id: kaiyo-1
      client-id: 07-tendermint-106
      connection-id: connection-76
    dst:
      chain-id: regen-1
      client-id: 07-tendermint-115
      connection-id: connection-104
    src-channel-filter:
      rule: "allowlist"
      channel-list:
        - channel-68
```

## Sommelier

[client Open](https://www.mintscan.io/sommelier/txs/CF99B798ED84C8EBCDC3160E2F4CA9C96EEC0C8D2C36F616DDDB92DBDDC941E4)  
[connection open](https://www.mintscan.io/sommelier/txs/DA9C39CF9FC2B8B562670CC0580886C222C5D46587ADB68FC61605D53B8D3D5A)  
[channel open](https://www.mintscan.io/sommelier/txs/48B72D1B5AF5858A277F38949A7FD94022E996C8E0DEA92AD158A198791AC476)

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: "defiantlabs"
  light-cache-size: 20
chains:
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
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
  sommelier:
    type: cosmos
    value:
      key: default
      chain-id: sommelier-3
      rpc-addr: https://rpc.sommelier.strange.love:443
      account-prefix: somm
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.01usomm
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      broadcast-mode: batch
paths:
  mainnet-kujira-sommelier:
    src:
      chain-id: kaiyo-1
      client-id: 07-tendermint-107
      connection-id: connection-77
    dst:
      chain-id: sommelier-3
      client-id: 07-tendermint-12
      connection-id: connection-8
    src-channel-filter:
      rule: "allowlist"
      channel-list:
        - channel-69
```
