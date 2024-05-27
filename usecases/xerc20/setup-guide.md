# Detailed Setup Guide

Hello! 👋 This section will guide you through the process of setting up your `xERC20` token.

## Prerequisites

Let's begin by getting a comprehensive understanding of the required steps based on your token's current situation.

#### 1. Categorize your token

Determine which of the following categories best describes your token's current state.

* **Category A**: The token is new and is not deployed anywhere.
* **Category B**: The token already exists on one chain.
* **Category C**: The token already exists on multiple chains.

{% hint style="info" %}
If you want to spin up an `xERC20` on testnet, the category may be different from your mainnet token. We recommend emulating your mainnet token setup if your goal is to testrun the process on testnet.\
\
For example: on mainnet, your token `TKN`is currently only deployed on Ethereum (**Category B**). Then on testnet, you should deploy a `TKN` to Goerli and follow the steps for a **Category B** token.
{% endhint %}

#### 2. Define your token's "home" chain

Based on your token's category:

* **Category A**: Choose one chain to be the home chain.&#x20;
* **Category B**: The chain where your token is currently deployed will be the home chain.&#x20;
* **Category C**: Choose one chain (among the ones your token is currently deployed) to be the home chain.

#### 3. Prepare to deploy tokens

* **Category A**:
  * You will deploy an `xERC20` on each chain you wish to support, including the home chain.
* **Category B** and **Category C**:
  * On each chain with an existing token, you need to figure out if a Lockbox setup is needed (next section).
  * On all other chains you wish to support, you will just deploy an `xERC20`.

## Lockbox Setup

A Lockbox allows any existing ERC20 to become compatible with the ERC-7281 (xERC20) standard. The Lockbox is just a simple wrapper contract, analogous to Wrapped ETH.

For **Category B** and **Category C**, there are tokens that already exist on certain chains. For each of these tokens, follow this flowchart to determine if you need to have a Lockbox setup on that token's chain.

<figure><img src="../../.gitbook/assets/xERC20_flowchart.png" alt=""><figcaption></figcaption></figure>

#### Example: NEXT token

To better understand how a Lockbox setup operates, consider the `NEXT` token as a real-world example.

* On Ethereum: Both the `NEXT` token and `xNEXT` token are deployed with a `Lockbox`.
* On Arbitrum: Only the `xNEXT` token is deployed.

Bridging from Ethereum to Arbitrum:

* \[Ethereum] User deposits `NEXT` into the Lockbox and receives `xNEXT`
* \[Ethereum] User calls the bridge using `xNEXT`&#x20;
* \[Arbitrum] Bridge delivers `xNEXT` to the user

Bridging from Arbitrum to Ethereum:

* \[Arbitrum] User calls the bridge using `xNEXT`
* \[Ethereum] Bridge withdraws `NEXT` from the Lockbox using the bridged `xNEXT`
* \[Ethereum] Bridge delivers `NEXT` to the user

## Deploying Contracts

Now that you have an idea of how your tokens should be set up, let's move on to the actual deployment procedures.&#x20;

#### xERC20s and Lockboxes

The Wonderland team provides an [xERC20 Github repository](https://github.com/defi-wonderland/xERC20/tree/main) that contains fully compliant implementations of `xERC20`, `Lockbox`, and scripts to deploy them. Factory contracts have already been deployed on each chain listed under `/broadcast/MultichainDeploy.sol/{chain_id}/run-latest.json`.

We suggest you deploy from a fork of this repo, please see the `README` for instructions. You will configure the scripts based on which chains you need to have Lockbox setups.

If you wish to roll your own version of an xERC20, make sure your custom implementation is compliant with the standard.

{% hint style="info" %}
The [ERC-7281](https://github.com/ethereum/EIPs/pull/7281) specification requires compliant tokens to implement ERC-20 along with mint/burn and some additional rate limit interfaces. The absolute _minimal_ interface needed is the ERC-20 interface plus mint/burn:

```solidity
/**
 * @notice Mints tokens for a user
 * @dev Can only be called by a bridge
 * @param _user The address of the user who needs tokens minted
 * @param _amount The amount of tokens being minted
 */
function mint(address _user, uint256 _amount) external;

/**
 * @notice Burns tokens for a user
 * @dev Can only be called by a bridge
 * @param _user The address of the user who needs tokens burned
 * @param _amount The amount of tokens being burned
 */
function burn(address _user, uint256 _amount) external;
```
{% endhint %}

#### LockboxAdapter

You might have noticed there's a `LockBoxAdapter` contract in the diagram above when you have a Lockbox setup. This contract facilitates the unwrapping of `xERC20 -> ERC20` on the destination chain and is needed for UIs to do this step automatically for users.

The Connext team has a `LockboxAdapter` deployed to all our supported chains (the implementation is available [here](https://github.com/connext/chain-abstraction-integration/blob/c35fbe757946cc76a826d93595cd99fd0db39c27/contracts/integration/LockboxAdapter.sol)).&#x20;

#### Whitelisting bridges

As the token issuer, you have the power to decide which bridges can mint/burn your token and the ability to set rate limits per bridge:

```
/**
 * @notice Updates the limits of any bridge
 * @dev Can only be called by the owner
 * @param _mintingLimit The updated minting limit we are setting to the bridge
 * @param _burningLimit The updated burning limit we are setting to the bridge
 * @param _bridge The address of the bridge we are setting the limits too
 */
function setLimits(address _bridge, uint256 _mintingLimit, uint256 _burningLimit) external;
```

These limits will replenish after`_DURATION` (by default the repo deploys `xERC20` with a value of 1 day).

Once your token is deployed, you can call `setLimits` to grant any bridge the privilege to mint/burn your token on that chain.

## Enabling Connext as a Bridge

If you want Connext to be able to bridge your token ([here's our pitch in the next section](how-xerc20-tokens-work-with-connext.md)), please go through the following steps.

1. Set rate limits for Connext.
   * For each chain where your xERC20 is deployed, call `setLimits` as the owner/governor. Use the appropriate Connext address listed under "Core Contract" [here](../../resources/deployments.md) as the `_bridge` parameter.
2. Submit a PR to our [ChainData mappings](https://github.com/connext/chaindata/blob/main/crossChain.json).
   *   For each chain where your xERC20 is deployed, add an object keyed by its address like this:

       ```json
       "0x4c781E4D22cfaAdA520cAe4aF9097C5ecf9C3A71": {
         "name": "xDappRadar",
         "symbol": "xRADAR",
         "decimals": 18
       }
       ```
3. Submit a PR to our [allowlisting scripts](https://github.com/connext/monorepo/blob/main/packages/deployments/contracts/src/cli/init/config/mainnet/production.ts).
   *   Under the `assets` key in the configuration object, add another object to the list like this:

       ```json
       {
         name: "RADAR",
         canonical: {
           domain: "11111",
           address: "0x202426c15a18a0e0fE3294415E66421891E2EB7C",
           decimals: 18,
         },
         representations: {
           /// ETHEREUM
           "6648936": {
             local: "0x202426c15a18a0e0fE3294415E66421891E2EB7C",
             adopted: "0x202426c15a18a0e0fE3294415E66421891E2EB7C",
           },
           /// BSC
           "6450786": {
             local: "0x489580eB70a50515296eF31E8179fF3e77E24965",
             adopted: "0x489580eB70a50515296eF31E8179fF3e77E24965",
           },
         },
       },
       ```
   * The `canonical` object should always have `11111` as the `domain`. Change the `address` and `decimals` to match your home chain xERC20. For example, `RADAR`'s home chain is Ethereum.
   * For each chain where your xERC20 is deployed (including the home chain), add an entry into the `representations` field keyed on the chain's `domainId`.&#x20;
     * [You can look up each chain's domainId here](broken-reference). We encourage commenting the chain name above each entry.
     * `local` and `adopted` should both be set to the xERC20 address. These exist as separate fields for non-xERC20 assets.
     * _Note: `domainId` is a Connext-specific identifier per chain that exists for forward compatibility with non-evm chains._

{% hint style="info" %}
📌 Please reference the ChainData PR in the allowlisting script PR to expedite the review process!
{% endhint %}

Once this is done, the Connext Labs team will review your PRs to sanity check deployment details. Once your PR is approved, your tokens will be whitelisted and transferrable across chains!

## Connextscan and Bridge UI Support

The Connext team will take care of listing your token on our [Bridge UI](https://bridge.connext.network) and be able to track transfers in the [Connext explorer](https://connextscan.io/).

## Router Liquidity

At this point, your token should be transferrable across chains with no added fees or slippage. However, because of how Connext’s model works, these transfers will happen in large batches through Ethereum L1 roughly once every 2-3 hours.

{% hint style="info" %}
💡 Learn more about [fast and slow path execution here](../../concepts/how-it-works/transaction-lifecycle.md).
{% endhint %}

If your usecase requires fast (i.e. <2 minute) transfers across chains, you will need some routers in our network to supply some liquidity to execute transactions immediately on behalf of users.

Please reach out to the Connext team and we can help work through options here with our router partners.
