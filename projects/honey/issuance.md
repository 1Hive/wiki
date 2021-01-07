---
description: >-
  Honey does not have a fixed supply, an issuance policy controls the rate at
  which Honey is minted over time.
---

# Issuance

Issuance refers to the process that mints new Honey. Honey is currently set to increase in supply at a rate of **30% per year.** As Honey is added to the supply it is put straight into the Common Pool, where it is available for distribution via proposals. The issuance rate can be adjusted via [decision proposals](decisions.md). 

The current issuance policy allows anyone to call a function to mint Honey to the common pool and the amount of Honey issued depends on the issuance rate parameter and number of blocks which has passed since the last time the function was called. Therefore the rate of compounding depends on how frequently this function is called.

It is worth noting that rate of issuance is an important and [controversial topic](https://forum.1hive.org/t/discussion-honey-issuance-policy/231) among the community and the general consensus is that the issuance policy should be modified. As a result of those ongoing discussions, work has been started by the [Luna Swarm](../../community/swarms/luna.md) to model and formally propose a [**dynamic issuance policy**](planned-improvements.md#dynamic-issuance-policy) to replace the current policy. 

{% hint style="info" %}
A formal decision proposal to adopt the dynamic issuance policy along with recommended parameterization is expected sometime in January 2021.
{% endhint %}

