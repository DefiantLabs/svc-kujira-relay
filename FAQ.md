# FAQ

## Kujira IBC Client Expiration

When a client expires, it looks like this:

```shell
rly q clients-expiration mainnet-kujira-crescent

client 07-tendermint-105 (kaiyo-1) is already expired (12 Jul 23 12:50 UTC)
client 07-tendermint-78 (crescent-1) expires in 264h7m9s (25 Jul 23 16:12 UTC)
```

This means the client watching crescent on Kujira kaiyo-1 is expired. You need to create a new one to be used as a placeholder - the substitute for the expired client.

```shell
rly tx client kujira crescent mainnet-kujira-crescent -d --override

2023-07-14T17:42:56.016002Z     info    Client Created  {"src_chain_id": "kaiyo-1", "src_client_id": "07-tendermint-145", "dst_chain_id": "crescent-1"}
```

Verify the client is created by querying all clients on Kujira. Look for the new client-id and ensure it has the correct counterparty chain-id.

```shell
rly q clients kujira | jq . > kuji-clients.json
grep -a4 '07-tendermint-145' kuji-clients.json

{
  "client_id": "07-tendermint-145",
  "client_state": {
    "@type": "/ibc.lightclients.tendermint.v1.ClientState",
    "chain_id": "crescent-1",
```

Craft a Kujira proposal. For the subject, use the expired client, and for the substitute, use the new client.

Subject client ID: `07-tendermint-105`

Substitute client ID: `07-tendermint-145`

File: `kujira-unexpire-client-07-tendermint-105-unsigned.json`

```json
{
  "body": {
    "messages": [
      {
        "@type": "/cosmos.gov.v1beta1.MsgSubmitProposal",
        "content": {
          "@type": "/ibc.core.client.v1.ClientUpdateProposal",
          "title": "swap_kujira_kaiyo_client",
          "description": "On 12 Jul 23 12:50 UTC, the Kujira client on crescent expired due to a monitoring issue and only one relayer, Defiant Labs, was participating in this path. Both of these issues have been resolved. The monitoring script has been updated and other relayers have committed to participating in this path.",
          "subject_client_id": "07-tendermint-105",
          "substitute_client_id": "07-tendermint-145"
        },
        "initial_deposit": [],
        "proposer": "kujira1x9fxqdkg4rumkzrck8t3qnhm30jgfsx9ntcpas"
      }
    ],
    "memo": "",
    "timeout_height": "0",
    "extension_options": [],
    "non_critical_extension_options": []
  },
  "auth_info": {
    "signer_infos": [],
    "fee": {
      "amount": [{"denom": "ukuji", "amount": "476"}],
      "gas_limit": "400000",
      "payer": "",
      "granter": ""
    }
  },
  "signatures": []
}
```

> **Note:** The fee amount needs to be exactly the `gas_limit` * `minimum-gas-prices` (as defined on the RPC node you broadcast the TX to). For example, if the `gas_limit` is `400000` and the `minimum-gas-prices` is `0.119ukuji`, then the fee amount needs to be exactly `476`.

Sign the transaction:

```shell
kujirad tx sign kujira-unexpire-client-07-tendermint-105-unsigned.json --from relayer --chain-id kaiyo-1 
```

Broadcast the TX:

```shell
kujirad tx broadcast kujira-unexpire-client-07-tendermint-105-signed.json
{"height":"0","txhash":"09B01F76AD6B5182E17D5B8AA96476F6D381A8A2FBBBEF3D2491B036C7159A41","codespace":"","code":0,"data":"","raw_log":"[]","logs":[],"info":"","gas_wanted":"0","gas_used":"0","tx":null,"timestamp":"","events":[]}
```

Verify the hash on Mintscan was successful: [Mintscan Link](https://www.mintscan.io/kujira/txs/09B01F76AD6B5182E17D5B8AA96476F6D381A8A2FBBBEF3D2491B036C7159A41)

Verify a proposal was created: [Proposal Link](https://www.mintscan.io/kujira/proposals/434)

Lastly, let the Kujira community know to vote on the proposal.