# Troubleshooting

## Honey Price Oracle

### Can't add liquidity for HNY when creating a Garden

When the Honey Price Oracle goes down, the price of HNY can't be fetched and users aren't able to add the $100 of liquidity for HNY needed to create a Garden.

If you suspect the oracle is down, you can check its health status on this page: &#x20;

* [https://health-status-umber.vercel.app/](https://health-status-umber.vercel.app/)

When the oracle goes down, there must be 24 hours of accurate observations after it syncs correctly before you can add liquidity for a new Garden. The Health Status page above will let you know if observations for the oracle are working correctly (Can Consult Prices: "Yes"), and when it will reach 24 hours of accurate observations.

If the oracle cannot consult prices (Can Consult Prices: "No"), or if you're unable to create a Garden after the oracle has 24 hours of accurate observations, please message the #gardens channel in Discord:  [https://discord.gg/5cBQseRthC](https://discord.gg/5cBQseRthC)

## xDai

### Something Went Wrong&#x20;

![](<../.gitbook/assets/image (6).png>)

If you see the above error here are the most common errors and their corresponding solution:

* **Transaction failed** on the faucet - 0.5 xDai needed.
* **Transport Status Error** - Clear cache and refresh browser
* ****[**Json RPC Error**](https://forum.1hive.org/t/troubleshooting-problems-on-metamask/215) - Use [alternate RPC](xdai.md#connecting-via-metamask)

### Still getting error&#x20;

Check [Unsupported chain error ](https://forum.1hive.org/t/troubleshooting-problems-on-metamask/215/33)
