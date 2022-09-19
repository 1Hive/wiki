---
description: A stablecoin Cross-Chain Bridge
---

# xPollinate

{% hint style="warning" %}
This bridge is currently in its beta phase, remember to use at your own risk.
{% endhint %}

xPollinate is a cross-chain bridge developed by Connext in collaboration with 1Hive.

Quoting directly from Connext's Documentation, the following is typically the main idea, which will in the future will enable cross-chain aggregation on Honeyswap as well:

_At a high level, Connext lets users swap **assetA** on **chainA** for **assetB** on **chainB** using conditional transfers. This happens in a few simple steps:_

_1._ _Alice, a user of Connext, sends a conditional transfer of **assetA** to Bob._

_2._ _Bob, a liquidity provider (aka a router), sends an equivalent amount of **assetB** to Alice._

_3._ _Alice unlocks her conditional transfer to receive **assetB**, which in turn allows Bob to do the same._

Therefore, in our Bridge, when users send DAI to the Router on Matic side of the Bridge, they will in return get the equivalent amount of xDai on the xDai side of the Bridge. Moreover, with this idea in mind, more bridges are planned to be built in order to allow Cross-Chain transactions, which will inevitably result in arbitrage opportunities for users.

It currently supports the transferring of DAI, USDC and USDT between the Polygon, xDai, Fantom and BSC mainnets.

## **How to Use xPollinate**

{% hint style="info" %}
If you run into any issues using the bridge, feel free to contact Connext support [here](https://support.connext.network/).
{% endhint %}

**Step 1** — Go to [xpollinate.io](https://xpollinate.io/) and connect your wallet to the chain yo want to transfer from.

_**Note:** Make sure to confirm that there's enough exit liquidity for the token and network you intend to bridge to._

![](<../.gitbook/assets/image (31).png>)

**Step 2** — Enter the Receiver's address (it can be the same address on the other chain, or you can choose a different address. Then press Swap.

![](<../.gitbook/assets/Sin título.png>)

**Step 3** — Sign in your wallet to confirm channel setup.

![](<../.gitbook/assets/image (34).png>)

**Step 4** — Enter the amount to transfer and confirm the Receiver Addres. Then press Swap.

![](<../.gitbook/assets/Sin título (2).png>)

**Step 5** — Confirm the transaction in your web3 wallet.

![](<../.gitbook/assets/Sin título (3).png>)

**Step 6** — As a precaution, the transaction must have 10+ confirmations before being sent on the other network. After it's completed you will see the following success message. You can click on the VIEW TX button to see the transaction in the Block Explorer.

![](<../.gitbook/assets/image (35).png>)

The following short video also explains how easy and fast it is to use the bridge:

{% embed url="https://youtu.be/RlcyBtz3R2w" %}
