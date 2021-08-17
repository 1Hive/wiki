# Farms on xDai

## xComb Token

**The xComb token is the local incentive token for Honeyswap on xDai.**

The value of xComb is derived from trading activity that occurs on Honeyswap on xDai through automated buybacks tied to swap fees. Half of the repurchased xComb tokens are burned, the other half recycled back into the Farming mechanism for future distribrution. The xComb token has a fixed supply, which will become deflationary as a result of half of the xComb buybacks being burned.

### xComb Supply and Emissions

The total fixed supply of xComb tokens is `1,000,000`. An initial airdrop of `5%` of the total fixed supply was airdropped to existing Honeyswap Liquidity providers proportional to the amount time and liquidity value contributed to Honeyswap prior to the airdrop. `10%` of airdropped tokens are immediately liquid, and the other `90%` are released continuously over `6 Months` .

The remaining `95%` of the xComb supply is scheduled to be distributed via farming over the course of `2 years`, the emission rate decays linearly such that by the end of the initial emmission period the rate is `25%` of the initial rate.

1% of the xComb emissions can be earned by referring people to the farms, encouraging people to integrate and promote the farms. The remainder of emissions are split between honeyswap pairs proportionally to their allocation points. Allocation points will be adjusted over time to curate the available liquidity in order to attract traders and maximize volume on the exchange. The following table shows the current distribution of allocation points among pairs:

| Pair | Points |
| :--- | :--- |
| xDAI-xComb | 20 |
| xDAI-HNY | 5 |
| xDAI-AGVE | 5 |
| HNY-AGVE | 3 |
| HNY-WETH | 3 |
| xDAI-STAKE | 2 |
| xDAI-LINK | 2 |
| WETH-WBTC | 2 |
| xDAI-WETH | 2 |
| USDC-xDAI | 1 |

The pairs included in the farms will be adjusted over time, a framework for evaluating and adding additional pairs is being worked on. Stay tuned!

## Governance

The Honeyswap AMM contracts are not upgradeable. Governance is limited to setting the fee receiver address.

The xComb token does not have any governance, it has a fixed supply and cannot be upgraded.

xComb farming contract is not upgradeable, but the xComb tokens held by the contract can be withdrawn to via governance in order to transition the farming rewards to a new contract. Governance of the farms has been split into two distinct roles using a wrapper contract.

**Manager:** Can add, remove, and adjust allocation points of pools.

**Admin**: Can change the manager address and initialize a migration by withdrawing xComb and unlocking all time-locked deposits.

Initially the [Tulip swarm multisig ](https://xdai.gnosis-safe.io/app/#/safes/0xD5a0d695589Fa9dEC023638b8dD24D71f051C63C/balances)will serve as the Manager, and 1Hive [Decisions](../honey/decisions.md) will control the Admin role.

## Farm Contracts

**xCombToken**: [`0x38Fb649Ad3d6BA1113Be5F57B927053E97fC5bF7`](https://blockscout.com/poa/xdai/address/0x38Fb649Ad3d6BA1113Be5F57B927053E97fC5bF7/read-contract)

**xCombFarm**: [`0xB44825cF0d8D4dD552f2434056c41582415AaAa1`](https://blockscout.com/poa/xdai/address/0xB44825cF0d8D4dD552f2434056c41582415AaAa1/read-contract)

**xCombFarm Governance Wrapper:** [`0xfBA19af3bE412E08AF9c7Cf60756d238D3cEAd25`](https://blockscout.com/poa/xdai/address/0xfBA19af3bE412E08AF9c7Cf60756d238D3cEAd25/read-contract)

**xCombAirdrop:** [`0xdD36008685108aFafc11F88bBc66C39A851Df843`](https://blockscout.com/poa/xdai/address/0xdD36008685108aFafc11F88bBc66C39A851Df843/read-contract)

**FeeReceiver:** [`0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7`](https://blockscout.com/xdai/mainnet/address/0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7/transactions)\`\`

### Subgraphs

[Farms Subgraph on xDai](https://api.thegraph.com/subgraphs/name/1hive/honeyfarm-xdai). Source code can be found [here](https://github.com/1Hive/honeyfarm-subgraph).



