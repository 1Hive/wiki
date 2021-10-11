# Honeyswap on Polygon

## Honeyswap Contracts and Deployment Info

### AMM Contracts

**Honeyswap Factory**: [`0x03DAa61d8007443a6584e3d8f85105096543C19c`](https://polygonscan.com/address/0x03DAa61d8007443a6584e3d8f85105096543C19c/contracts#code)****

**Honeyswap Router**: [`0xaD340d0CD0B117B0140671E7cB39770e7675C848`](https://polygonscan.com/address/0xaD340d0CD0B117B0140671E7cB39770e7675C848/contracts#code)

**ReferralRewardReceiver**: [`0xf72e8827aa4c03e2c49aa95a6550dd4c8a65a969`](https://polygonscan.com/address/0xf72e8827aa4c03e2c49aa95a6550dd4c8a65a969#code)``

**FeeReceiver**: [`0xA25958B0C9bbEE1821dB5CE3d85bc56848Fddf78`](https://polygonscan.com/address/0xA25958B0C9bbEE1821dB5CE3d85bc56848Fddf78#code)

### Subgraphs

[Honeyswap Subgraph on Polygon](https://api.thegraph.com/subgraphs/name/1hive/honeyswap-polygon). Source code can be found [here](https://github.com/1Hive/honeyswap-subgraph).

### Honeymaker

[Honeymaker](https://github.com/1hive/honeymaker) is an accompanying bot that periodically calls the `takeProtocolFee()` function on the FeeReceiver contract for selected pairs on Honeyswap to convert the LP fees earned to Honey and pComb.
