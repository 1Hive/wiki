---
description: >-
  Honey is minted and burned automatically to stabilize the ratio between
  circulating supply and the common pool reserve.
---

# Suministro

The total supply of Honey fluctuates as it is automatically minted and burned from the common pool reserves. Therefore, Honey does not have a fixed total supply. However, token supply adjustments follow a policy which makes them predictable and allows them to be projected out based on simple assumptions about inflows and outflows to the common pool. 

The policy will mint Honey, increasing the supply, when the common pool balance is less than 30% of the total supply. It will burn Honey, reducing the supply, when the common pool balance is above 30% of the supply. Adjustments will be made proportionally to the distance from the target ratio, however adjustments will not exceed the throttle rate of 10% per year in either direction. 

### Policy 

[This is the deployed contract](https://blockscout.com/poa/xdai/address/0x783Da66eeA5a93F46F386806Fce49Ce18937F861/read-proxy) which manages supply adjustments. The policy is intended to operate without governance intervention indefinitely but it can be upgraded and its parameters changed via a [Decision](). Anyone can call the `executeAdjustment()` function, which will check the last time the function was called and mint or burn the appropriate amount of Honey to/from the common pool.

It is encouraged for people who are interested in understanding the mechanism to carefully review the [solidity implementation](https://github.com/1Hive/issuance/blob/master/contracts/Issuance.sol) as well as the [research summary and mechanism proposal](https://forum.1hive.org/t/dynamic-honey-supply-policy-proposal/2224). However, the policy can be summarized as follows:

Adjustments to the supply are calculated using a proportional control function where the further from the target ratio the system is the greater the magnitude of adjustment are.

```text
error = (1 - current_ratio / target_ratio) / seconds_per_year
```

This `error` term tells us how much we should be adjusting the supply to get back to the target ratio. The `seconds_per_year` constant smooths the adjustments so that even though we can adjust on a per block basis, it would take approximately a year \(all else equal\) for the system to get back to the target ratio.

To ensure that we can provide a simple and easy to understand upper bound on how quickly the total supply can change over time, we limit the magnitude of any adjustment by a throttle parameter.

```text
error = (1 - current_ratio / target_ratio) / seconds_per_year

if error < 0:
	adjustment = max(error, -throttle) * supply
else:
  adjustment = min(error, throttle) * supply 
```

In practice the throttle is an artificial limit on the ability for the mechanism to adjust supply, if the throttle kicks in it will take longer for the system to reach the target ratio and may reach an equilibrium that is higher or lower than desired. 

The two important parameters of the policy are set to the following values. 

| Parameter | Value | Notes |
| :--- | :--- | :--- |
| targetRatio | 3000000000 | Fractional ratio value multiplied by RATIO\_PRECISION in contract \(1e10\) eg a target ratio of 30% or **0.3** would be 3e9 |
| maxAdjustmentRatioPerSecond | 3170979198 | A max adjustment ratio \(throttle\) of 10% or **0.1** would be 0.1 / 31536000 \(seconds in year\) = 0.000000003170979198 multiplied by EXTRA\_PRECISION in contract \(1e18\) = 3170979198 |

### Automation

There is not currently any automation to ensure that the `executeAdjustment()` function is called regularly. However, anyone is welcome to call it and can do so by clicking the honey logo on the `1hive.org` frontend. 

