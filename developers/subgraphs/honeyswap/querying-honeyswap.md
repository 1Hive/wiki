# Querying Honeyswap

You can build your own queries using a [GraphQL Explorer](https://graphiql-online.com/graphiql) and enter your endpoint to limit the data to exactly what you need.

Each entity has a plural version and a singular version. When querying for a single record response (e.g. account), you will need to supply the id for the entity. When querying for a list of responses (e.g. accounts), you may add filters using the ‘where’ clause.

Below are some sample queries you can use to gather information from the Honeyswap contracts.

### Example <a href="#example" id="example"></a>

#### This query fetches aggredated data from all honeyswap pairs and tokens, to give a view into how much activity is happening within the whole protocol <a href="#this-query-fetches-aggredated-data-from-all-honeyswap-pairs-and-tokens-to-give-a-view-into-how-much" id="this-query-fetches-aggredated-data-from-all-honeyswap-pairs-and-tokens-to-give-a-view-into-how-much"></a>

```
{
  honeyswapFactories(first: 1) {
    pairCount
    totalVolumeUSD
    totalLiquidityUSD
  }
}
```

#### Returns <a href="#returns" id="returns"></a>

```
{
  "data": {
    "honeyswapFactories": [
      {
        "pairCount": 1929,
        "totalVolumeUSD": "423698337.853415549849554234184245",
        "totalLiquidityUSD": "11432873.66895439928443725337007973"
      }
    ]
  }
}
```

#### This query fetches aggredated data and returns the first 5 factories and tokens associated <a href="#this-query-fetches-aggredated-data-and-returns-the-first-5-factories-and-tokens-associated" id="this-query-fetches-aggredated-data-and-returns-the-first-5-factories-and-tokens-associated"></a>

```

  honeyswapFactories(first: 5) {
    id
    pairCount
    totalVolumeUSD
    totalVolumeNativeCurrency
  }
  tokens(first: 5) {
    id
    symbol
    name
    decimals
  }
```

#### Result <a href="#result" id="result"></a>

```
{
  "data": {
    "honeyswapFactories": [
      {
        "id": "0xa818b4f111ccac7aa31d0bcc0806d64f2e0737d7",
        "pairCount": 276,
        "totalVolumeUSD": "43846497.23378379329008972499525061",
        "totalVolumeNativeCurrency": "43846497.23378379329008972499525061"
      }
    ],
    "tokens": [
      {
        "id": "0x01f4a4d82a4c1cf12eb2dadc35fd87a14526cc79",
        "symbol": "UNI-V2",
        "name": "Uniswap V2",
        "decimals": "18"
      },
      {
        "id": "0x0a5e0895cb83cf77fc8ab35c416adb39ac861c0b",
        "symbol": "SEGL",
        "name": "Segal Family",
        "decimals": "18"
      },
      {
        "id": "0x0a9446f538288124e0c67425e3ff513203a98ce0",
        "symbol": "YFTP",
        "name": "ToiletPaper.Finance on xDai",
        "decimals": "18"
      },
      {
        "id": "0x0acd91f92fe07606ab51ea97d8521e29d110fd09",
        "symbol": "CEL",
        "name": "Celsius on xDai",
        "decimals": "4"
      },
      {
        "id": "0x0da1a02cdf84c44021671d183d616925164e08aa",
        "symbol": "REN",
        "name": "Republic Token on xDai",
        "decimals": "18"
      }
    ]
  }
}
```
