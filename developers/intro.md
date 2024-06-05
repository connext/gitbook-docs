# Introduction

Connext provides the simplest possible experience for building xchain applications (**xApps**).

Building a xApp requires only two straightforward steps:

1. Implement `xReceive` in the destination chain contract. This is the function that receives the payload you pass across chains.
2. Call `xcall` on the origin chain, passing in your payload and relayer fees.

Get started with the [Quickstart](quickstart.md)!

***

## Important Concepts

### Fast Path vs. Slow Path

Take a moment to review the [Transaction Lifecycle](../concepts/how-it-works/transaction-lifecycle.md). Here we introduce the concept of "fast path" and "slow path" (authenticated) transfers. The differentiation is crucial to understand for any cross-chain project. Then, try it out with our [Authentication guide](guides/authentication.md).

### Relayer Fees

Check out our [guide on relayer fees](guides/estimating-fees.md) and how to estimate them.

### Handling Failures

You should always build in contingency for [failed calls](guides/handling-failures.md).

### Tracking xCalls

Dive into the c[urrent status of an `xcall`](guides/xcall-status.md).

### Nested xCalls

You can even [chain `xcall`](guides/nested-xcalls.md)`s` across domains! :open\_mouth:

### Chain Abstraction

Create [seamless cross-chain interactions](../usecases/chain-abstraction/chain-abstraction-guide.md) without having to switch chains! 🤯

***

## Help

Have questions or need support? Our core team and vibrant community members are highly active in our Discord server!

[Chat with us!](https://discord.gg/everclear)
