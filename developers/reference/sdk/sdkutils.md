# SdkUtils

SDK class encapsulating utility functions.

## Hierarchy

*   `SdkShared`

    ↳ **`SdkUtils`**

## Methods

### getRoutersData

▸ **getRoutersData**(): `Promise`<`any`>

Fetches a list of router liquidity data.

**Returns**

`Promise`<`any`>

Array of objects containing the router address and liquidity information, in the form of:

```ts
{
  "address": "0xf26c772c0ff3a6036bddabdaba22cf65eca9f97c",
  "asset_canonical_id": "0x000000000000000000000000a0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
  "asset_domain": "1869640809",
  "router_address": "0xf26c772c0ff3a6036bddabdaba22cf65eca9f97c",
  "balance": 8816006545,
  "local": "0x67e51f46e8e14d4e4cab9df48c59ad8f512486dd",
  "adopted": "0x7f5c764cbc14f9669b88837ca1490cca17c31607",
  "canonical_id": "0x000000000000000000000000a0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
  "canonical_domain": "6648936",
  "domain": "1869640809",
  "key": "0x6d9af4a33ed4034765652ab0f44205952bc6d92198d3ef78fe3fb2b078d0941c",
  "id": "0x67e51f46e8e14d4e4cab9df48c59ad8f512486dd",
  "fees_earned": 7249237
}
```

***

### getTransfers

▸ **getTransfers**(`params`): `Promise`<`any`>

Fetches the transfers that match filter criteria.

**Parameters**

| Name                      | Type                   |
| ------------------------- | ---------------------- |
| `params`                  | `Object`               |
| `params.range?`           | `Object`               |
| `params.range.limit?`     | `number`               |
| `params.range.offset?`    | `number`               |
| `params.routerAddress?`   | `string`               |
| `params.status?`          | `XTransferStatus`      |
| `params.transactionHash?` | `string`               |
| `params.transferId?`      | `string`               |
| `params.userAddress?`     | `string`               |
| `params.errorStatus?`     | `XTransferErrorStatus` |

**Returns**

`Promise`<`any`>

The object containing transfer data in the form of:

```ts
{
  "transfer_id": "0x4a379d3367bb589ddc00dd7c2d7d6557bed75c9595e5cd6a4369d85e587ec386",
  "nonce": 34,
  "to": "0x6d2a06543d23cc6523ae5046add8bb60817e0a94",
  "call_data": "0x",
  "origin_domain": "6778479",
  "destination_domain": "6648936",
  "receive_local": false,
  "origin_chain": "100",
  "origin_transacting_asset": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
  "origin_transacting_amount": "100000000000000",
  "origin_bridged_asset": "0x538e2ddbfdf476d24ccb1477a518a82c9ea81326",
  "origin_bridged_amount": "99407526243394",
  "xcall_caller": "0x6d2a06543d23cc6523ae5046add8bb60817e0a94",
  "xcall_transaction_hash": "0xd1b4f723c1f7453bc38e8dd64f56830ed1e907b95c8b5eba55a9f1a26d867ea8",
  "xcall_timestamp": 1672964955,
  "xcall_gas_price": "4654771330",
  "xcall_gas_limit": "511921",
  "xcall_block_number": 25819530,
  "destination_chain": "1",
  "status": "CompletedFast",
  "routers": [
    "0xf26c772c0ff3a6036bddabdaba22cf65eca9f97c"
  ],
  "destination_transacting_asset": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
  "destination_transacting_amount": "99357822480272",
  "destination_local_asset": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
  "destination_local_amount": "99407526243394",
  "execute_caller": "0x75c6a865c30da54e365cb5def728890b3dd8bdc4",
  "execute_transaction_hash": "0x7e02bd79087ec48d9588f655474ba7f38921b46ab8ff812f2b2a8b97bad9fa72",
  "execute_timestamp": 1672965155,
  "execute_gas_price": "32181349289",
  "execute_gas_limit": "4000000",
  "execute_block_number": 16344186,
  "execute_origin_sender": "0x6d2a06543d23cc6523ae5046add8bb60817e0a94",
  "reconcile_caller": "0xf7c4d7dcec2c09a15f2db5831d6d25eaef0a296c",
  "reconcile_transaction_hash": "0xe3c8042bcd2e943df1d3a38c75bfee132827f3a8a3a1efedf1e4e96cecd72e6b",
  "reconcile_timestamp": 1672986047,
  "reconcile_gas_price": "19184906166",
  "reconcile_gas_limit": "4000000",
  "reconcile_block_number": 16345915,
  "update_time": "2023-01-12T04:56:14.72407",
  "delegate": "0x6d2a06543d23cc6523ae5046add8bb60817e0a94",
  "message_hash": "0x327618edf7bab0e7c6b97ecee50ad6572e9c069a85db3083c942e0c0ddc469b7",
  "canonical_domain": "6648936",
  "slippage": 300,
  "origin_sender": "0x6d2a06543d23cc6523ae5046add8bb60817e0a94",
  "bridged_amt": "99407526243394",
  "normalized_in": "100000000000000",
  "canonical_id": "0x000000000000000000000000c02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
  "router_fee": null,
  "xcall_tx_origin": "0x6d2a06543d23cc6523ae5046add8bb60817e0a94",
  "execute_tx_origin": "0x29d33fcd30240d55b9280362599d5066c1a2cf10",
  "reconcile_tx_origin": "0x29d33fcd30240d55b9280362599d5066c1a2cf10",
  "relayer_fee": "8424181656635272573"
}
```

***

### create

▸ `Static` **create**(`_config`): `Promise`<`SdkUtils`>

Create a singleton instance of the SdkUtils class.

**Parameters**

| Name                    | Type                                                                                   | Default value | Description                                             |
| ----------------------- | -------------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------- |
| `_config`               | `Object`                                                                               | undefined     | SdkConfig object.                                       |
| `_config.chains`        | `Record`<`string`, { providers: string\[] }>                                           | undefined     | Chain config, at minimum with providers for each chain. |
| `_config.signerAddress` | `string`                                                                               | undefined     | Signer address for transactions.                        |
| `_config.logLevel`      | `"fatal"` \| `"error"` \| `"warn"` \| `"info"` \| `"debug"` \| `"trace"` \| `"silent"` | "info"        | (optional) Logging severity level.                      |
| `_config.network`       | `"testnet"` \| `"mainnet"`                                                             | "mainnet"     | (optional) Blockchain environment to interact with.     |

**Returns**

`Promise`<`SdkUtils`>

providers.TransactionRequest object.

**`Example`**

```ts
import { SdkUtils } from "@connext/sdk";

const config = {
  signerAddress: "<wallet_address>",
  network: "mainnet",
  chains: {
    6648936: { // the domain ID for Ethereum Mainnet
      providers: ["https://rpc.ankr.com/eth"],
    },
    1869640809: { // the domain ID for Optimism
      providers: ["https://mainnet.optimism.io"]
    },
    1886350457: { // the domain ID for Polygon
      providers: ["https://polygon-rpc.com"]
    },
  },
}

const sdkBase = await SdkUtils.create(config);
```

{% hint style="info" %}
See the [Deployments](broken-reference) page for all domain IDs and asset addresses.
{% endhint %}
