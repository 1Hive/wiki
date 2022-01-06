---
description: >-
  Honeyswap is network of decentralized exchanges which are supported and
  maintained by the 1Hive community.
---

# Honeyswap

## Overview

Honeyswap is comprised of liquidity pool contracts deployed to multiple EVM compatible chains which share common frontend interfaces that are maintained by the 1Hive community. Currently Honeyswap supports xDai and Polygon, but plans to expand support to other EVM chains and rollups in the future.&#x20;

Honeyswap uses a **multi-token model** to manage the balance between **Global** and **Local** incentives. Development, support, and maintainence work that has **Global** benefits are funded using **Honey** from 1Hive's common pool. Farming Rewards, where benefits are localized to a one supported chain use a **Comb token** which can be valued as a derivative of the volume on that specific chain.

Swap fees on Honeyswap are split 1/12 to Honey, 1/12 to the local Comb token for that chain, and 5/6 directly to the pool of liquidity providers facilitating the swap.

{% hint style="info" %}
**Trades with ETH on Polygon have a fee of only 0.15%**
{% endhint %}

## Honeyswap Frontend

The [Honeyswap frontend](https://app.honeyswap.org) provides an open source interface for trading and pooling liquidity. It also supports routing trades to third-party liquidity pools so that users can be sure they are getting the best trade execution when they choose to interact using Honeyswap's frontend.&#x20;

You can connect to Honeyswap from any supported chain, and will be able to interact with the pool on that network.&#x20;

## Honeyswap Analytics&#x20;

[Honeyswap Analytics](https://info.honeyswap.org)  provides an open source interface for analyzing liquidity, volume, and trading history.

## Honeyswap Governance

The Honeyswap AMM contracts are not upgradeable. Governance is limited to setting the fee reciever address.

## Honeycomb Asset Manager&#x20;

[Honeycomb](../honeycomb/) provides an open source interface for managing DeFi positions, including depositing and withdrawing from Comb farms.
