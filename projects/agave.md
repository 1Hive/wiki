---
description: Lending protocol
---

# Agave

{% hint style="warning" %}
This page reflects the [initial Agave proposal](https://forum.1hive.org/t/announcing-agaave-aave-on-xdai/1792). Agave is still under development and this page may still be incomplete or inaccurate.
{% endhint %}

## Overview

Agave is a decentralized non-custodial money market protocol where users can participate as depositors or borrower. It is a fork of [Aave](https://aave.com/) deployed on xDAI.

Depositors provide liquidity to the market to earn a passive income, while borrowers can borrow in an overcollateralized (perpetually) or undercollateralized (one-block liquidity) fashion (i.e., flash loans).

### How does it work?

Users deposit tokens into the protocol, they receive an aToken token in return. This aToken then accrues interest. Further, when depositing, users can enable their deposit to be used as collateral and use this to borrow other assets. This is functionally equivalent to offering leverage facility. For example, if a user deposits `HNY`, they can then use that as collateral to borrow `DAI` and buy more `HNY`.

## Capabilities

### Lending

Users can lend tokens to the protocol. Interest is determined dynamically by the Utilization rate of the token in the protocol. So as the supply of the token decreases, the interest rate increases

### Borrowing

Once a user lends to the protocol, they have a line of credit they can use to borrow against. The

### Delegate Borrowing

Lenders can extend their line of credit to other addresses. This effectively gives opens the possibility for users who have nothing deposited in Agave to lend from the protocol without capital.

### Flash Loans

Agave flash loans are more powerful than most offered on mainnet. Users are able to borrow multiple tokens in the same transaction. Additionally, Flash loans in Agave do not need to be totally paid back in the same transaction: Some of the loan can be added as debt if the user has enough collateral in the protocol.

## Token

Agave has a token primarily used for governance over the protocol.

* Adding/removing tokens from the market
* Enabling/disabling the ability to use specific tokens as collateral
* Setting the collateral rates
* Maximum LTV (loan to value rate)
* Liquidation threshold
* Liquidation penalty
* Used as collateral
* Stable borrowing

The token is also stakeable, giving `AGAVE` holders the ability to earn a yield on the `AGAVE` token itself. The pool of staked tokens is used as insurance in the case of a shortfall event.

## How does this benefit 1Hive?

Currently, we have Honeyswap, which allows users to trade on xDAI with super low transaction fees. Given the relatively low volume, the total fees generated in HoneySwap (0.3% per trade) are rather low, and as such we have subsidized liquidity providers by allowing them to farm `HNY`. This has had mixed results.

With Agave, we would enable users to earn a yield on regular HoneySwap Liquidity tokens without a `HNY` subsidy. It also adds extra incentives to liquidity providers by giving them an additional stream of income above the fees generated on HoneySwap.

One of the most powerful features of DeFi is its composability. Currently, HoneySwap is not composable with the other DeFi protocols because it is on a separate chain. With Agave, we will now have another protocol on xDAI making it more ‘sticky’.

Although we will be forking Aave, we will use this as a base for a protocol that fits the needs of the 1Hive community.

Token listing on Agave will be more frictionless than Aave. Using Celeste, anyone can add a token to the Agave market by staking the Agave token, if a token does not meet the associated [Aragon Agreement](https://aragon.org/agreements) it can be challenged with Celeste.

These are some ways that Agave will provide `HNY` more utility as well as increase the price of `HNY`.
