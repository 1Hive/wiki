---
description: Using the xDai sidechain.
---

# xDai

The **xDai sidechain** is a stable payments blockchain designed for fast and inexpensive stable transactions. **xDai** is used for transactions, payments and fees, and **STAKE** is used to support Proof-of-Stake consensus.

See the [xDai documentation](https://www.xdaichain.com/) for more details.

## Connecting via MetaMask

See [this guide](https://www.xdaichain.com/for-users/wallets/metamask/metamask-setup) from the xDai documentation to connect your [MetaMask](https://metamask.io/) extension to the xDai chain.

**Alternative RPCs:**

* [https://dai.poa.network/](https://dai.poa.network/) 
* [https://xdai.poanetwork.dev/](https://xdai.poanetwork.dev/)  
* [https://xdai.1hive.org/](https://xdai.1hive.org/) 
* [https://rpc.xdaichain.com/](https://rpc.xdaichain.com/)

## xDai Faucet

For anyone interested in experimenting with xDai before bridging tokens from the Ethereum mainnet, you can use the xDai faucet to claim 0.01 xDai \(~ 1 cent\) for free, which is enough to execute a few transactions on xDai. Anyone can top-up the xDai faucet balance.

{% embed url="https://xdai-faucet.top/" %}

## Bridging Tokens from Ethereum

To convert DAI on the Ethereum network to xDai that lives on the xDai network use the [dai-bridge](https://dai-bridge.poa.network/).

To convert ERC20 tokens on the Ethereum network to ERC20 tokens on the xDai network use the [omnibridge](https://xdai-omnibridge.web.app/).

## Bridging Tokens from other Sidechains

To transfer stablecoins between sidechains using the [xPollinate](https://xpollinate.io/) bridge, which uses [Connext](https://connext.network)'s State Channels, a technology that enables bridging without introducing any new trust assumptions or external validators.

Currently supports the transferring of DAI, USDC and USDT between the Polygon, xDai, Fantom and BSC mainnets.

{% page-ref page="xpollinate.md" %}

## Other Info

Ensure that no matter what MetaMask sets your gas cost to, that you always set it to 1. xDai gas cost is always 1 Gwei, paying less than this it's unlikely your transaction will be accepted, paying more than this will waste xDai. The gas limit should typically be left as it is.

The xDai [Block Explorer](https://blockscout.com/poa/xdai), similar to Etherscan, can be used to see transactions and accounts.

If you need help getting connected or using any of the above services, come to the [`#⛈help`](https://discord.gg/3AjG7XvRJZ)Discord channel.

