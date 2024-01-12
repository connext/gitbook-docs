# SdkShared

SDK class encapsulating shared logic to be inherited.

## Hierarchy

*   **`SdkShared`**

    ↳ `SdkBase`

    ↳ `SdkRouter`

    ↳ `SdkPool`

    ↳ `SdkUtils`

## Methods

### approveIfNeeded

▸ **approveIfNeeded**(`domainId`, `assetId`, `amount`, `infiniteApprove?`): `Promise`<`undefined` | `TransactionRequest`>

Returns the transaction request for an allowance approval.

**Parameters**

| Name              | Type      | Default value | Description                                       |
| ----------------- | --------- | ------------- | ------------------------------------------------- |
| `domainId`        | `string`  | `undefined`   | The domain ID.                                    |
| `assetId`         | `string`  | `undefined`   | The address of the token.                         |
| `amount`          | `string`  | `undefined`   | The amount of the token.                          |
| `infiniteApprove` | `boolean` | `true`        | (optional) Whether to approve an infinite amount. |

**Returns**

`Promise`<`undefined` | `TransactionRequest`>

providers.TransactionRequest object.

***

### calculateCanonicalKey

▸ **calculateCanonicalKey**(`domainId`, `canonicalId`): `string`

Returns the hash of the canonical ID + canonical domain.

**`Remarks`**

This key is used as the unique identifier for a canonical token, across all domains.

**Parameters**

| Name          | Type     | Description                           |
| ------------- | -------- | ------------------------------------- |
| `domainId`    | `string` | The canonical domain ID of the token. |
| `canonicalId` | `string` | The canonical ID of the token.        |

**Returns**

`string`

***

### changeSignerAddress

▸ **changeSignerAddress**(`signerAddress`): `Promise`<`void`>

Switches the signer address in the SDK config.

**Parameters**

| Name            | Type     | Description             |
| --------------- | -------- | ----------------------- |
| `signerAddress` | `string` | The new signer address. |

**Returns**

`Promise`<`void`>

***

### getAssetsData

▸ **getAssetsData**(): `Promise`<`AssetData`\[]>

Fetches the list of registered assets.

**Returns**

`Promise`<`AssetData`\[]>

Array of objects containing assets registered to the network, in the form of:

```ts
{
  "local": "0x2983bf5c334743aa6657ad70a55041d720d225db",
  "adopted": "0x82af49447d8a07e3bd95bd0d56f35241523fbab1",
  "canonical_id": "0x000000000000000000000000c02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
  "canonical_domain": "6648936",
  "domain": "1634886255",
  "key": "0x12acadfa38ab02479ae587196a9043ee4d8bf52fcb96b7f8d2ba240f03bcd08a",
  "id": "0x2983bf5c334743aa6657ad70a55041d720d225db"
},
```

***

### getAssetsDataByDomainAndKey

▸ **getAssetsDataByDomainAndKey**(`domainId`, `key`): `Promise`<`undefined` | `AssetData`>

Retrieve the asset data for a specific domain and key.

**Parameters**

| Name       | Type     | Description                                |
| ---------- | -------- | ------------------------------------------ |
| `domainId` | `string` | The domain ID.                             |
| `key`      | `string` | The canonical hash of the canonical token. |

**Returns**

`Promise`<`undefined` | `AssetData`>

The object containing asset data.

***

### getCanonicalTokenId

▸ **getCanonicalTokenId**(`domainId`, `tokenAddress`): `Promise`<\[`string`, `string`]>

Returns the canonical ID and canonical domain of a token.

**Parameters**

| Name           | Type     | Description                           |
| -------------- | -------- | ------------------------------------- |
| `domainId`     | `string` | The canonical domain ID of the token. |
| `tokenAddress` | `string` | The address of the token.             |

**Returns**

`Promise`<\[`string`, `string`]>

***

### getSupported

▸ **getSupported**(): `Promise`<`ConnextSupport`\[]>

Fetches the list of supported networks and assets.

**Returns**

`Promise`<`ConnextSupport`\[]>

Array of objects containing networks and assets supported by the protocol, in the form of:

```ts
{
  "name": "arbitrum",
  "chainId": 42161,
  "domainId": "1634886255",
  "assets": [
    "0x82af49447d8a07e3bd95bd0d56f35241523fbab1",
    "0xff970a61a04b1ca14834a43f5de4533ebddb5cc8"
  ]
},
```

***

### isNextAsset

▸ **isNextAsset**(`tokenAddress`): `Promise`<`undefined` | `boolean`>

Returns whether the specified token is a Connext-issued (local) token.

**Parameters**

| Name           | Type     | Description               |
| -------------- | -------- | ------------------------- |
| `tokenAddress` | `string` | The address of the token. |

**Returns**

`Promise`<`undefined` | `boolean`>

Boolean or undefined if the specified token is not registered.

***

### parseConnextTransactionReceipt

▸ **parseConnextTransactionReceipt**(`transactionReceipt`): `any`

Parses a providers.TransactionReceipt for the logs.

**Parameters**

| Name                 | Type                 | Description                          |
| -------------------- | -------------------- | ------------------------------------ |
| `transactionReceipt` | `TransactionReceipt` | providers.TransactionReceipt object. |

**Returns**

`any`

Array of providers.Log objects.

***

### domainToChainName

▸ `Static` **domainToChainName**(`domainId`): `string`

Returns the chain name for a specified domain.

**Parameters**

| Name       | Type     | Description    |
| ---------- | -------- | -------------- |
| `domainId` | `string` | The domain ID. |

**Returns**

`string`

The chain name.

***

### chainIdToDomain

▸ `Static` chainIdToDomain(`chainId`): `number`

Returns the chain name for a specified domain.

**Parameters**

| Name      | Type     | Description    |
| --------- | -------- | -------------- |
| `chainId` | `number` | The domain ID. |

**Returns**

`number`

The domain of the chain.

***

### getBlockNumberFromUnixTimestamp

▸ `Static` **getBlockNumberFromUnixTimestamp**(`domainId`, `unixTimestamp`): `Promise`<`number`>

Uses an external API to fetch the block number from a unix timestamp.

**Parameters**

| Name            | Type     | Description         |
| --------------- | -------- | ------------------- |
| `domainId`      | `string` | The domain ID.      |
| `unixTimestamp` | `number` | The unix timestamp. |

**Returns**

`Promise`<`number`>
