# For Liquidity Providers

## Liquidity Provider Return on Investment (ROI)

Liquidity providers are rewarded 0.25% and every swap is proportionally distributed to the liquidity providers of that exchange pair.

Liquidity providers experience impermanent loss when providing liquidity. Any temporary loss becomes permanent when liquidity is removed from the pool.

Liquidity providers are profitable when collected fees > impermanent loss.

The ROI for providing liquidity is highest when the ratio of liquidity to volume is high, and the pair of assets are highly correlated.&#x20;

## Impermanent Loss

Impermanent loss is a temporary loss of funds occurring when providing liquidity. It’s very often explained as a difference between holding an asset versus providing liquidity in that asset. Impermanent loss is usually observed in standard liquidity pools where the liquidity provider has to provide both assets in a correct ratio, and one of the assets is volatile in relation to the other.

In the example of an wETH/xDAI 50/50 pair if wETH goes up in value, the pool has to rely on arbitrageurs continually ensuring that the pool price reflects the real-world price to maintain the same value of both tokens in the pool. This basically leads to a situation where profit from the token that appreciated in value is taken away from the liquidity provider. At this point, if the LP decides to withdraw their liquidity, the impermanent loss becomes permanent.

## Liquidity Farming

In the past we deployed liquidity farms at [hny.farm](http://hny.farm). Liquidity providers of Honeyswap exchange pairs could stake their LP tokens to the Honey Farms in return for Honey (funded by proposals) to encourage keeping liquidity in Honeyswap. However, the general consensus amongst the community was that the Honey farms weren't worth maintaining so they haven't continued to be funded.
