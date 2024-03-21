# Configuration

The router is accepts configuration using the config file `config.json` in the root directory of the [docker-compose repo](https://github.com/connext/router-docker-compose).

The JSON schema accepts the following keys:

* `redis`: _Required_. Object containing the following keys to configure an external redis instance:
  * `host`: _Required_. The hostname of the redis instance.
  * `port`: _Required_. The port of the redis instance.
* `server`: _Required_. Object containing the following keys to configure the HTTP server:
  * `adminToken`: _Required_. Secret token used to authenticate admin requests.
  * `port`: _Optional_. The port the router will listen on. Defaults to `8080`.
  * `host`: _Optional_. The host the router will listen on. Defaults to `0.0.0.0`.
* `web3SignerUrl`: _Recommended_. The URL for a running [Web3Signer](https://docs.web3signer.consensys.net/en/latest/) instance. This is the recommended approach to private key storage.
* `mnemonic`: _Optional, Discouraged_. The mnemonic used to generate the private key. Using the mnemonic directly in the config file is unsafe and not recommended.
* `chains`: _Required_. The chain configuration. A JSON object with the following keyed by Domain IDs with the following object schema as value:
  * `providers`: _Required_. An array of providers URLs for a chain. Use a minimum of 1 URL, but additional URLs provide more fallback protection against provider issues.
  * `assets`: _Required_. An array of assets. Each asset is a JSON object with the following keys:
    * `assetId`: _Required_. The asset ID (ERC20 token address). This needs to represent the "local" asset which is the Connext bridge minted asset.
    * `name`: _Required_. The Asset Name.
* `network`: _Required_. `mainnet` or `testnet`.
* `environment`: _Optional_. `production` or `staging`. `mainnet` network config will always be `production`.
* `logLevel`: _Optional_. The log level. Defaults to `info`. Accepts `debug`, `info`, `warn`, `error`, `fatal`, `trace`, `silent`.
* `sequencerUrl`: _Optional_. The URL for the sequencer. Only used to override defaults.
* `cartographerUrl`: _Optional_. The URL for the cartographer. Only used to override defaults.

## Example Configuration File

_These are example RPC URLs. Please get your own RPC URLs!_

```json
{
  "chains": {
    "1634886255": {
      "assets": [
        {
          "address": "0x8c556cF37faa0eeDAC7aE665f1Bb0FbD4b2eae36",
          "name": "USDC"
        },
        {
          "address": "0x2983bf5c334743Aa6657AD70A55041d720d225dB",
          "name": "WETH"
        }
      ],
      "providers": [
        "https://arb-mainnet.g.alchemy.com/v2/...",
        "https://rpc.ankr.com/arbitrum"
      ]
    },
    "1869640809": {
      "assets": [
        {
          "address": "0x67E51f46e8e14D4E4cab9dF48c59ad8F512486DD",
          "name": "USDC"
        },
        {
          "address": "0xbAD5B3c68F855EaEcE68203312Fd88AD3D365e50",
          "name": "WETH"
        }
      ],
      "providers": [
        "https://opt-mainnet.g.alchemy.com/v2/...",
        "https://rpc.ankr.com/optimism"
      ]
    },
    "1886350457": {
      "assets": [
        {
          "address": "0xF96C6d2537e1af1a9503852eB2A4AF264272a5B6",
          "name": "USDC"
        },
        {
          "address": "0x4b8BaC8Dd1CAA52E32C07755c17eFadeD6A0bbD0",
          "name": "WETH"
        }
      ],
      "providers": [
        "https://polygon-mainnet.g.alchemy.com/v2/...",
        "https://rpc.ankr.com/polygon"
      ]
    },
    "6450786": {
      "assets": [
        {
          "address": "0x5e7D83dA751F4C9694b13aF351B30aC108f32C38",
          "name": "USDC"
        },
        {
          "address": "0xA9CB51C666D2AF451d87442Be50747B31BB7d805",
          "name": "WETH"
        }
      ],
      "providers": [
        "https://bsc-dataseed1.binance.org",
        "https://bsc-dataseed2.binance.org",
        "https://rpc.ankr.com/bsc"
      ]
    },
    "6648936": {
      "assets": [
        {
          "address": "0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48",
          "name": "USDC"
        },
        {
          "address": "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
          "name": "WETH"
        }
      ],
      "providers": [
        "https://eth-mainnet.alchemyapi.io/v2/...",
        "https://rpc.ankr.com/eth"
      ]
    },
    "6778479": {
      "assets": [
        {
          "address": "0x44CF74238d840a5fEBB0eAa089D05b763B73faB8",
          "name": "USDC"
        },
        {
          "address": "0x538E2dDbfDf476D24cCb1477A518A82C9EA81326",
          "name": "WETH"
        }
      ],
      "providers": [
        "https://rpc.gnosischain.com",
        "https://rpc.ankr.com/gnosis"
      ]
    }
  },
  "environment": "production",
  "logLevel": "debug",
  "messageQueue": {
    "uri": "amqp://guest:guest@rabbitmq:5672"
  },
  "redis": {
    "host": "redis",
    "port": 6379
  },
  "server": {
    "adminToken": "supersecret"
  },
  "web3signer": "http://signer:9000",
  "network": "mainnet"
}
```
