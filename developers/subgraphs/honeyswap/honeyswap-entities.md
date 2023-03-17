# Honeyswap Entities

* [`HoneyswapFactory`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#honeyswapfactory)
* [`Token`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#token)
* [`Pair`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#pair)
* [`User`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#user)
* [`LiquidityPosition`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#liquidityposition)
* [`LiquidityPositionSnapshot`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities)
* [`Transaction`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#transaction)
* [`Mint`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#mint)
* [`Burn`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#burn)
* [`Swap`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#swap)
* [`Bundle`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#bundle)
* [`HoneyswapDayData`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities)
* [`PairHourData`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#pairhourdata)
* [`PairDayData`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#pairdaydata)
* [`TokenDayData`](https://hackmd.io/@GraphSubgraphDocs/Honeyswap-Entities#tokendaydata)

### HoneyswapFactory <a href="#honeyswapfactory" id="honeyswapfactory"></a>

Description: Contains data across all of Honeyswap. This entity tracks important things like total liquidity (in ETH and USD, see below), all time volume, transaction count, number of pairs and more.

| Field                        | Type        | Description                                  |
| ---------------------------- | ----------- | -------------------------------------------- |
| id                           | ID!         | Factory id                                   |
| pairCoint                    | Int!        | Pair info                                    |
| totalVolumeUSD               | BigDecimal! | Total volume                                 |
| totalVolumeNativeCurrency    | BigDecimal! | Total volume in native currency              |
| untrackedVolumeUSD           | BigDecimal! | Untracked values - less confident USD scores |
| totalLiquidityUSD            | BigDecimal! | Total liquidity                              |
| totalLiquidityNativeCurrency | BigDecimal! | Total liquidity in native currency           |
| txCount                      | BigInt!     | Transactions                                 |

### Token <a href="#token" id="token"></a>

Description: Contains data on a specific token. This token specific data is aggregated across all pairs, and is updated whenever there is a transaction involving that token.

| Field                 | Type              | Description                            |
| --------------------- | ----------------- | -------------------------------------- |
| id                    | ID!               | Token address                          |
| symbol                | String!           | Token symbol from smart contract       |
| name                  | String!           | Token name from smart contract         |
| decimals              | BigInt!           | Token decimals from the smart contract |
| totalSupply           | BigInt!           | Used for other stats like marketcap    |
| tradeVolume           | BigDecimal!       | Token specific trade volume            |
| tradeVolumeUSD        | BigDecimal!       | Token specific trade volume in usd     |
| untrackedVolumeUSD    | BigDecimal!       | Token specific untracked volume in usd |
| txCount               | BigInt!           | Transactions across all pairs          |
| totalLiquidity        | BigDecimal!       | Liquidity across all pairs             |
| derivedNativeCurrency | BigDecimal        | Derived native currency                |
| tokenDayData          | \[TokenDayData!]! | Token day data                         |
| pairDayDataBase       | \[PairDayData!]!  | Token pair day data base               |
| pairDayDataQuote      | \[PairDayData!]!  | Token pair day data quote              |
| pairBase              | \[Pair!]!         | Token pair base                        |
| pairQuote             | \[Pair!]!         | Token pair quote                       |

### Pair <a href="#pair" id="pair"></a>

Description: Contains data on a specific pair.

| Field                        | Type                           | Description                                      |
| ---------------------------- | ------------------------------ | ------------------------------------------------ |
| id                           | ID!                            | Pair id                                          |
| token0                       | Token!                         | Token 0                                          |
| token1                       | Token!                         | Token 1                                          |
| reserve1                     | BigDecimal!                    | Pair reserve                                     |
| totalSupply                  | BigDecimal!                    | Total supply                                     |
| reserveNativeCurrency        | BigDecimal!                    | Reserve native currency                          |
| reserveUSD                   | BigDecimal!                    | Reserve amount in usd                            |
| trackedReserveNativeCurrency | BigDecimal!                    | Used for separating per pair reserves and global |
| token0Price                  | BigDecimal!                    | Price in terms of the asset pair                 |
| token1Price                  | BigDecimal!                    | Price in terms of the asset pair                 |
| volumeToken0                 | BigDecimal!                    | Lifetime volume stats                            |
| volumeToken1                 | BigDecimal!                    | Lifetime volume stats                            |
| volumeUSD                    | BigDecimal!                    | Lifetime volume stats                            |
| untrackedVolumeUSD           | BigDecimal!                    | Lifetime volume stats                            |
| txCount                      | BigInt!                        | lifetime volume stats                            |
| createdAtTimestamp           | BigInt!                        | Timestamp pair was created                       |
| createdAtBlockNumber         | BigInt!                        | Blocknumber pair was created                     |
| liquidityProviderCount       | BigInt!                        | Used to detect new exchanges                     |
| pairHourData                 | \[PairHourData!]!              | Pair hour data                                   |
| liquidityPositions           | \[LiquidityPosition!]!         | Pair liquididty posistions                       |
| liquidityPositionSnapshots   | \[LiquidityPositionSnapshot!]! | Snapshot of liquididty position                  |
| mints                        | \[Mint!]!                      | Token pairs minted                               |
| burns                        | \[Burn!]!                      | Token pairs burned                               |
| swaps                        | \[Swap!]!                      | Token pair swaps                                 |

### User <a href="#user" id="user"></a>

Description: get specific details of the User

| Field              | Type                  | Description               |
| ------------------ | --------------------- | ------------------------- |
| id                 | ID!                   | User id                   |
| liquidityPositions | \[LiquidityPosition!] | Users liquididty position |
| usdSwapped         | BigDecimal!           | USD value of swapped      |

### LiquidityPosition <a href="#liquidityposition" id="liquidityposition"></a>

Description: get specific details of the Liquidity Position

| Field                 | Type        | Description             |
| --------------------- | ----------- | ----------------------- |
| id                    | ID!         | Liquidity position id   |
| user                  | User!       | User liquidity position |
| pair                  | Pair!       | Pair liquidity position |
| liquidityTokenBalance | BigDecimal! | Token balance of LP     |

### LiquidityPositionSnapshot <a href="#liquiditypositionsnapshot" id="liquiditypositionsnapshot"></a>

Description: get specific details of the Liquidity Position Snapshot

| Field                     | Type               | Description                          |
| ------------------------- | ------------------ | ------------------------------------ |
| id                        | ID!                | liquidity position snapshot id       |
| liquidityPosition         | LiquidityPosition! | Snapshot of LP position              |
| timestamp                 | Int!               | Saved for fast historical lookups    |
| block                     | Int!               | Saved for fast historical lookups    |
| user                      | User!              | Reference to user                    |
| pair                      | Pair!              | Reference to pair                    |
| token0PriceUSD            | BigDecimal!        | Snapshot of token0 price             |
| token1PriceUSD            | BigDecimal!        | Snapshot of token1 price             |
| reserve0                  | BigDecimal!        | Snapshot of pair token0 reserves     |
| reserve1                  | BigDecimal!        | Snapshot of pair token1 reserves     |
| reserveUSD                | BigDecimal!        | Snapshot of pair reserves in USD     |
| liquidityTokenTotalSupply | BigDecimal!        | Snapshot of pool token supply        |
| liquidityTokenBalance     | BigDecimal!        | Snapshot of users pool token balance |

### Transaction <a href="#transaction" id="transaction"></a>

Description: Every transaction on Honeyswap is stored. Each transaction contains an array of mints, burns, and swaps that occured within it.

| Field       | Type     | Description                     |
| ----------- | -------- | ------------------------------- |
| id          | ID!      | Txn hash                        |
| blockNumber | BigInt!  | Blocknumber of transaction      |
| timestamp   | BigInt!  | Timestamp of transaction        |
| mints       | \[Mint]! | Used to track incomplete mints  |
| burns       | \[Burn]! | Used to track incomplete burns  |
| swaps       | \[Swap]! | Used to track incompleted swaps |

### Mint <a href="#mint" id="mint"></a>

Description: These contain specifc information about a transaction. Things like which pair triggered the transaction, amounts, sender, recipient, and more. Each is linked to a parent Transaction entity.

| Field        | Type         | Description                                                    |
| ------------ | ------------ | -------------------------------------------------------------- |
| id           | ID!          | Transaction hash + “-” + index in mints Transaction array      |
| transaction  | Transaction! | Transaction has of mint                                        |
| timestamp    | BigInt!      | Need this to pull recent txns for specific token or pair       |
| pair         | Pair!        | Address of pair                                                |
| to           | Bytes!       | Populated from the primary Transfer event                      |
| liquidity    | BigDecimal!  | Populated from the primary Transfer event                      |
| sender       | Bytes        | Populated from the Mint event                                  |
| amount0      | BigDecimal   | Populated from the Mint event                                  |
| amount1      | BigDecimal   | Populated from the Mint event                                  |
| logIndex     | BigInt       | Populated from the Mint event                                  |
| amountUSD    | BigDecimal   | Derived amount based on available prices of tokens             |
| feeTo        | Bytes        | Optional fee fields, if a Transfer event is fired in \_mintFee |
| feeLiquidity | BigDecimal   | Optional fee fields, if a Transfer event is fired in \_mintFee |

### Burn <a href="#burn" id="burn"></a>

Description: These contain specifc information about a transaction. Things like which pair triggered the transaction, amounts, sender, recipient, and more. Each is linked to a parent Transaction entity.

| Field         | Type         | Description                                                    |
| ------------- | ------------ | -------------------------------------------------------------- |
| id            | ID!          | Transaction hash + “-” + index in mints Transaction array      |
| transaction   | Transaction! | Transaction hash of burn                                       |
| timestamp     | BigInt!      | Need this to pull recent txns for specific token or pair       |
| pair          | Pair!        | Address of pair                                                |
| liquidity     | BigDecimal!  | Populated from the primary Transfer event                      |
| sender        | Bytes        | Populated from the Burn event                                  |
| amount0       | BigDecimal   | Populated from the Burn event                                  |
| amount1       | BigDecimal   | Populated from the Burn event                                  |
| to            | Bytes        | Populated from the Burn event                                  |
| logIndex      | BigInt       | Populated from the Burn event                                  |
| amountUSD     | BigDecimal   | Derived amount based on available prices of tokens             |
| needsComplete | Boolean!     | Mark uncomplete in ETH case                                    |
| feeTo         | Bytes        | Optional fee fields, if a Transfer event is fired in \_mintFee |
| feeLiquidity  | BigDecimal   | Optional fee fields, if a Transfer event is fired in \_mintFee |

### Swap <a href="#swap" id="swap"></a>

Description: These contain specifc information about a transaction. Things like which pair triggered the transaction, amounts, sender, recipient, and more. Each is linked to a parent Transaction entity.

| Field       | Type         | Description                                               |
| ----------- | ------------ | --------------------------------------------------------- |
| id          | ID!          | Transaction hash + “-” + index in mints Transaction array |
| transaction | Transaction! | Pointer to transaction                                    |
| timestamp   | BigInt!      | Need this to pull recent txns for specific token or pair  |
| pair        | Pair!        | Address of pair                                           |
| sender      | Bytes!       | Populated from the Swap event                             |
| from        | Bytes!       | The EOA that initiated the txn                            |
| amount0In   | BigDecimal!  | Amount of token0 swapped in                               |
| amount1In   | BigDecimal!  | Amount of token1 swapped in                               |
| amount0Out  | BigDecimal!  | Amount of token0 swapped out                              |
| amount1Out  | BigDecimal!  | Amount of token1 swapped out                              |
| to          | Bytes!       | Address swapped to                                        |
| logIndex    | BigInt       | Order within the txn                                      |
| amountUSD   | BigDecimal!  | Amount of swap in USD                                     |

### Bundle <a href="#bundle" id="bundle"></a>

Description: get specific details of the bundle

| Field               | Type        | Description                  |
| ------------------- | ----------- | ---------------------------- |
| id                  | ID!         | Bundle address               |
| nativeCurrencyPrice | BigDecimal! | Price of native currency usd |

### HoneyswapDayData <a href="#honeyswapdaydata" id="honeyswapdaydata"></a>

Description: get specific details of the honeyswap day data

| Field                        | Type        | Description                                                                                                                   |
| ---------------------------- | ----------- | ----------------------------------------------------------------------------------------------------------------------------- |
| id                           | ID!         | Timestamp rounded to current day by dividing by 86400                                                                         |
| date                         | Int!        | Date of information                                                                                                           |
| dailyVolumeNativeCurrency    | BigDecimal! | Daily volume in native currency                                                                                               |
| dailyVolumeUSD               | BigDecimal! | Daily volume in USD                                                                                                           |
| dailyVolumeUntracked         | BigDecimal! | Daily volume                                                                                                                  |
| totalVolumeNativeCurrency    | BigDecimal! | Total volume in native currency                                                                                               |
| totalLiquidityNativeCurrency | BigDecimal! | Total liquidity in native token                                                                                               |
| totalVolumeUSD               | BigDecimal! | Accumulate at each trade, not just calculated off whatever totalVolume is. making it more accurate as it is a live conversion |
| totalLiquidityUSD            | BigDecimal! | Total liquidity in USD                                                                                                        |
| txCount                      | BigInt!     | Transactions across all pairs                                                                                                 |

### PairHourData <a href="#pairhourdata" id="pairhourdata"></a>

Description: get specific details of the pair hour data

| Field              | Type        | Description                      |
| ------------------ | ----------- | -------------------------------- |
| id                 | ID!         | Pair hour data id                |
| hourStartUnix      | Int!        | Unix timestamp for start of hour |
| pair               | Pair!       | Address of pair                  |
| reserve0           | BigDecimal! | Reserves                         |
| reserve1           | BigDecimal! | Reserves                         |
| reserveUSD         | BigDecimal! | Derived liquidity                |
| hourlyVolumeToken0 | BigDecimal! | Hourly volume token0             |
| hourlyVolumeToken1 | BigDecimal! | Hourly volume token1             |
| hourlyVolumeUSD    | BigDecimal! | Hourly volume in usd             |
| hourlyTxns         | BigInt!     | Number of hourly trasactions     |

### PairDayData <a href="#pairdaydata" id="pairdaydata"></a>

Description: get specific details of the pair day data

| Field             | Type        | Description                            |
| ----------------- | ----------- | -------------------------------------- |
| id                | ID!         | Pair day data id                       |
| date              | Int!        | Date of information                    |
| pairAddress       | Bytes!      | Address of pair                        |
| token0            | Token!      | Token0 address                         |
| token1            | Token!      | Token1 address                         |
| reserve0          | BigDecimal! | Reserves                               |
| reserve1          | BigDecimal! | Reserves                               |
| totalSupply       | BigDecimal! | Total supply for LP historical returns |
| reserveUSD        | BigDecimal! | Derived liquidity                      |
| dailyVolumeToken0 | BigDecimal! | Daily volume token0                    |
| dailyVolumeToken1 | BigDecimal! | Daily volume token1                    |
| dailyVolumeUSD    | BigDecimal! | Daily volume in usd                    |
| dailyTxns         | BigInt!     | Number of daily transactions           |

### TokenDayData <a href="#tokendaydata" id="tokendaydata"></a>

Description: get specific details of the token day data

| Field                        | Type        | Description                     |
| ---------------------------- | ----------- | ------------------------------- |
| id                           | ID!         | Token day data id               |
| date                         | Int!        | Date of information             |
| token                        | Token!      | Token symbol                    |
| dailyVolumeToken             | BigDecimal! | Token daily volume              |
| dailyVolumeNativeCurrency    | BigDecimal! | Daily volume native currency    |
| dailyVolumeUSD               | BigDecimal! | Daily volume in usd             |
| dailyTxns                    | BigInt!     | Number of daily transactions    |
| totalLiquidityToken          | BigDecimal! | Total amount for liqidity token |
| totalLiquidityNativeCurrency | BigDecimal! | Total liquidity native currency |
| totalLiquidityUSD            | BigDecimal! | Total liquidity usd             |
| priceUSD                     | BigDecimal! | Price usd                       |
