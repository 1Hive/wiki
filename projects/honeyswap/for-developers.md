# For Developers

## HoneySwap

HoneySwap is a modified deployment of UniSwap on xDai.

### Contracts

**UniswapV2Factory**:[`0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7`](https://blockscout.com/poa/xdai/address/0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7)\*\*\*\*

**UniswapV2Router02**:[`0x1C232F01118CB8B424793ae03F870aa7D0ac7f77`](https://blockscout.com/poa/xdai/address/0x1C232F01118CB8B424793ae03F870aa7D0ac7f77)

### Front-end

The front-end is deployed at [honeyswap.org](https://honeyswap.org) and the source code can be found [here](https://github.com/1Hive/uniswap-interface). The major modifications are rebranding and a modified token list set.

### Info.honeyswap.org

A uniswap.info fork for Honeyswap. It can be viewed at [info.honeyswap.org](https://info.honeyswap.org).

### Subgraphs

The fork is powered by forks of two subgraphs:

[Uniswap v2 Subgraph](https://thegraph.com/explorer/subgraph/1hive/uniswap-v2): A fork of the official Uniswap v2 subgraph with adjustments to use xDai as the base currency and a modified set of whitelisted tokens. Source code can be found [here](https://github.com/1Hive/uniswap-v2-subgraph).

[Ethereum Blocks](https://thegraph.com/explorer/subgraph/1hive/xdai-blocks): A fork of the Blocklytics Ethereum Blocks subgraph with no modifications, deployed for xDai. Source code can be found [here](https://github.com/1Hive/ethereum-blocks).

### Front-end

The front-end is a fork of the official uniswap.info source code with modifications to use Blockscout instead of Etherscan along with minor adjustments to use the appropriate token lists and factory addresses.

 The source code for the front-end can be found [here](https://github.com/1Hive/uniswap-info/).

### Honeymaker

Honeymaker is a SushiMaker deployment and accompanying bot that converts LP shares on Honeyswap into Honey for the Honey Common Pool.

SushiMaker is deployed at [`0x076b64f9F966e3bBD0FCdC79D490Ab71cF961bb0`](https://blockscout.com/poa/xdai/address/0x076b64f9F966e3bBD0FCdC79D490Ab71cF961bb0).

The bot periodically calls the `convert` function on the SushiMaker contract for selected pairs on Honeyswap to convert the LP shares to Honey.

The source code for the bot can be found [here](https://github.com/1hive/honeymaker).

### Useful Links

The [Common pool](https://thegraph.com/explorer/subgraph/onbjerg/honey) Subgraph.

