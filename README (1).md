---
description: Key Details, Token Allocation, and Eligibility Criteria
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Airdrop Details

{% hint style="warning" %}
This document is currently subject to public review before being finalized. If you notice a revision that needs to be made or have feedback, please [request a revision](https://github.com/connext/gitbook-docs/issues/new) or start a conversation with us on Discord at [https://discord.com/invite/everclear](https://discord.com/invite/everclear)
{% endhint %}

## Airdrop Overview

The NEXT airdrop will be conducted through a first-of-its-kind airdrop mechanism, allowing eligible recipients to natively claim NEXT on the chain of their choice without the need to use a bridge or pay unnecessary gas fees.

### NEXT Details

<table><thead><tr><th width="231"></th><th>Details</th></tr></thead><tbody><tr><td>Total supply</td><td>1,000,000,000</td></tr><tr><td>Token type</td><td>xERC20</td></tr><tr><td>Token address</td><td><a href="https://etherscan.io/address/0xFE67A4450907459c3e1FFf623aA927dD4e28c67a">0xFE67A4450907459c3e1FFf623aA927dD4e28c67a</a></td></tr><tr><td>Claimable chains</td><td>Arbitrum, Optimism, Polygon, and Gnosis Chain</td></tr><tr><td>Snapshot date</td><td>August 1, 2023 at 00:00 UTC<br>Timestamp: 1690848000</td></tr><tr><td>Claiming begins</td><td>September 05, 2023 at 13:00 UTC<br>Timestamp: 1693918800</td></tr><tr><td>Claiming ends</td><td>March 05, 2024 at 13:00 UTC<br>Timestamp: 1714914000</td></tr></tbody></table>

***

### Airdrop Eligibility Criteria

{% tabs %}
{% tab title="Users" %}
{% hint style="info" %}
After carefully reviewing feedback, we found that certain categories of transactions were not being counted towards the airdrop as we originally intended.

\
To provide the best possible outcome, we adjusted the eligibility criteria on August 24, 2023. The total amount of NEXT that will be distributed during the airdrop was increased, ensuring that no pre-existing allocations are decreased.
{% endhint %}

A basic point system was used to determine the number of NEXT each recipient can claim. Our points criteria accounted for stableswap liquidity provision and bridge usage, with the most points awarded to users demonstrating consistent usage. In total, a maximum of 13 points were possible with both bridge and LP activity, and using partner projects or being a community advocate acted as a multiple on the accumulated points.

### User Qualifying Criteria

Users earn 1pt for meeting the Mandatory Qualifiers and 1pt for each qualifier unless otherwise stated.

#### Mandatory Qualifiers

_Users must qualify for at least one of the following two criteria in order to qualify for the NEXT airdrop_

1. Transferred 5 or more times with an average value of at least $15 per transaction (calculated across all transactions) and a total volume exceeding $200.
2. Provided at least $1,500 in liquidity to the Connext network for a minimum of 1 day.

_Vector usage will be included towards your points if_

1. Users interacted with NXTP (deployed November 2021) at least once via bridging or LPing.

#### Stableswap LP Activity Qualifiers

1. Interacted with stableswap pools at least 25 times.
2. Interacted with stableswap pools at least 50 times.
3. Interacted with stableswap pools at least 100 times.
4. Provided at least $3,000 in liquidity (2 pts).
5. Provided at least $6,000 in liquidity (2 pts).
6. Provided at least $9,000 in liquidity (2 pts).
7. Provided at least $12,000 in liquidity (2 pts).
8. Provided liquidity for at least 30 days.
9. Provided liquidity for at least 60 days.

#### Bridge Usage Qualifiers

1. 10 or more bridge transactions.
2. 25 or more bridge transactions.
3. 50 or more bridge transactions.
4. At least 3 unique months.
5. At least 6 unique months.
6. At least 9 unique months.
7. At least 12 unique months.
8. Transacted at least $1,000 on v2.
9. Transacted at least $2,500 on v2.
10. Transacted at least $5,000 on v2.
11. Transferred between 6 or more chains.
12. Transferred between 10 or more chains.

#### Multipliers

1. Utilized a partner protocol (1.5x Multiplier)
{% endtab %}

{% tab title="Routers" %}
A basic point system was used to determine the number of NEXT each router has earned. Our points criteria focused primarily on utility of provided capital, with longevity carve-outs to recognize the importance of capital being available on relatively low traffic chains. Additionally, multipliers were applied to router operators that were exceptionally helpful to the community (created dashboards, ran subgraph infrastructure, etc.) as well as those impacted by the nomad hack.

### Router Qualifying Criteria

#### Router Activity Qualifiers

1. Had transactions in at least 7 unique months.
2. Had transactions in at least 12 unique months.
3. More than 50K transactions.
4. More than 200K transactions.
5. More than 350K transactions.
6. More than $5M in total router volume.
7. More than $40M in total router volume.
8. More than $80M in total router volume.
9. More than 100 days of transaction support.
10. More than 400 days of transaction support.
11. More than 700 days of transaction support.

#### Multipliers

1. Impacted by nomad hack (1.5x multiplier).
2. Contributing router operators (3x multiplier).
{% endtab %}

{% tab title="Community Advocates" %}
A basic point system was used to determine the number of NEXT each CA / CL earned. Our points criteria focused on quality and duration of contributions

### Community Advocate Qualifying Criteria

#### Mandatory Qualifiers

* Must be an active leader in the Connext community as recognized by the team.

#### Community Advocate Activity Qualifiers

* Number of months of support
* Quality of contributions
{% endtab %}
{% endtabs %}

***

### Sybil Filtering

To mitigate Sybil attacks, the following filters were applied to the data:

* _**Removal of Known Malicious Actors.**_ \
  Addresses associated with previous Sybil attempts or known hackers were eliminated from the data.
* _**Interaction Analysis.**_ \
  The interaction amount, frequency, and volume were analyzed across Ethereum, Polygon, and Binance Smart Chain (BNB). Addresses matching identified sybil-patterns (suspiciously high amounts of activity, identical transfer types, etc.) were eliminated from the airdrop.
* _**Fund Flow Analysis.**_\
  Addresses that share a funding source may indicate Sybil accounts.
* _**Address Clustering.**_\
  Transaction graphs were analyzed using clustering and community detection algorithms to identify sybils.

***
