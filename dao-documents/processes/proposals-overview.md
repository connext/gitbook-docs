---
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

# Proposals Overview

{% hint style="warning" %}
This document is currently subject to public review before being finalized. If you notice a revision that needs to be made or have feedback, please [request a revision](https://github.com/connext/gitbook-docs/issues/new) or start a conversation with us on Discord at [https://discord.com/invite/everclear](https://discord.com/invite/everclear)
{% endhint %}

## **Types of Proposals**

There are three main types of governance proposals you can make:

1. **Executable Proposal:** \
   This is a proposal for a series of smart contract operations to be executed by accounts the DAO controls. These can include transfers of tokens as well as arbitrary smart contract calls. Examples of this include allocating funding to a workstream multisig wallet or upgrading the Connext core contract. To maintain the security of the protocol, the proposed code must be audited by a high-quality third-party auditor and reviewed by the Security Council. Executable proposals have a quorum requirement of 15 million NEXT tokens and require a minimum approval of 50% to pass.&#x20;
2. **Social Proposal:** \
   This proposal seeks the consensus of the DAO members on a matter that cannot be implemented or enforced via on-chain mechanisms. Social proposals have a quorum requirement of 15 million NEXT tokens and require a minimum approval of 50% to pass.
3. **Constitutional Amendment:** \
   This is a social proposal that asks the DAO to amend the constitution. The draft proposal should include the exact changes proposed to be made to the constitution. A quorum of 36 million is currently required, and a minimum approval of two-thirds to pass.

***

## **Phases of Proposal**

### **Phase 1: Request for Comments**

_A governance forum post providing a description of a proposal._

#### To create a Request for Comment:

* Ask a general, non-biased question to the community on the forum about a potential change. Forum posts should be labeled as follows: “Request for Comment - \[Your Title Here]“.
* Reach out to your network to build support for the proposal. Discuss the proposal and solicit delegates to provide feedback on it. Be willing to respond to questions and comments. Share your viewpoint, but try to remain impartial.

{% hint style="info" %}
**Note**: The length of this phase is limited to 7 days. It’s in the proposal author’s interest to get as much feedback from the community as possible in this limited period of time.
{% endhint %}

{% hint style="info" %}
**Temperature Check:** Temperature check was removed from the process based on [Formal Vote - Social CGP1 - Voting Duration](https://snapshot.org/#/dao.connext.eth/proposal/0x77125238d344e5e378387d048d6e3b2c2a45bf3d3d2b6c22b1b76c443e4e9301).
{% endhint %}

### **Phase 2: Formal Vote**

_A final governance forum post incorporating any feedback from the Request for Comments phase._\
_The proposal in this phase should include the following sections:_ [_Connext Governance Proposal Template_](connext-governance-proposal-template.md)

#### To Create a Formal Vote:

1. Navigate to the relevant RFC and post a comment that the formal vote is live. Include the relevant title “Formal Vote \[Social/Constitutional/Executable \[Proposal Number]] — \[Your Title Here]” and link to any relevant Snapshot polls/discussion threads. Proposal numbers should be in a “CGP#” format. Topics that begin with “Formal Vote” that have not successfully passed Request for Comment stages should be removed by community moderators.
2. Ensure at least 600,000 NEXT is delegated to your address in order to submit a proposal or find a delegate who has enough delegated NEXT to meet the proposal threshold and propose on your behalf.
   * **Social Proposal or Constitutional Amendment:** \
     Navigate to Snapshot and schedule the proposal for a snapshot vote. Votes are delayed by 2 days, and voting lasts for 7 days. If the snapshot vote passes, the proposal is passed, and you are done!
   * **Executable Proposal:**\
     Generate the transaction using the Connext Zodiac module. If the transaction is not cross-chain, the SAFE transaction builder can be used to generate the executable data. Submit the proposal to a vote via Snapshot transaction builder. Votes are delayed by 2 days, voting lasts for 7 days, and “For,” “Abstain,” and “Against” are the voting options. If the proposal passes, anyone can request execution via Snapshot UI. Requesters must post a 5 WETH bond, and there is a 3-day delay. Once the delay elapses, anyone can execute the proposal via Snapshot, which will return the bond to the requester and execute on-chain transaction.

{% hint style="info" %}
**Note**: SAFE admins retain authority to delete proposals and submit their own multisig transactions, serving as a security council with veto power on community votes. \
More information about the Security Council is available [here](https://docs.connext.network/v/dao-documentation/collective/security-council).
{% endhint %}

{% hint style="info" %}
**Note:** Voting Duration was changed to 7 days + delays, based on [Formal Vote - Social CGP1 - Voting Duration](https://snapshot.org/#/dao.connext.eth/proposal/0x77125238d344e5e378387d048d6e3b2c2a45bf3d3d2b6c22b1b76c443e4e9301).
{% endhint %}

