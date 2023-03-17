# Querying Gardens

You can build your own queries using a [GraphQL Explorer](https://graphiql-online.com/graphiql) and enter your endpoint to limit the data to exactly what you need.

Each entity has a plural version and a singular version. When querying for a single record response (e.g. account), you will need to supply the id for the entity. When querying for a list of responses (e.g. accounts), you may add filters using the ‘where’ clause.

Below are some sample queries you can use to gather information from the Gardens contracts.

### Examples <a href="#examples" id="examples"></a>

#### This example shows how to query a list of Gardens <a href="#this-example-shows-how-to-query-a-list-of-gardens" id="this-example-shows-how-to-query-a-list-of-gardens"></a>

```
query Organizations(
  $first: Int!
  $skip: Int!
  $orderBy: String!
  $orderDirection: String!
) {
  organizations(
    first: $first
    where: { active: true }
    skip: $skip
    orderBy: $orderBy
    orderDirection: $orderDirection
  ) {
    id
    active
    createdAt
    proposalCount
    token {
      id
      symbol
      name
      decimals
    }
    wrappableToken {
      id
      symbol
      name
      decimals
    }
    honeyLiquidity
    supporterCount
    incentivisedPriceOracle
    unipool
  }
}
```

#### Returns <a href="#returns" id="returns"></a>

```
  "data": {
    "courtConfigs": [
      {
        "id": "0x44e4fcfed14e1285c9e0f6eae77d5fdd0f196f85",
        "currentTerm": "2187",
        "termDuration": "28800",
        "feeToken": {
          "id": "0x71850b7e9ee3f13ab46d67167341e4bdc905eef9"
        }
      }
    ],
    "courtTerms": [
      {
        "id": "0",
        "startTime": "1614960796",
        "randomnessBN": "0",
        "randomness": "0x0000000000000000000000000000000000000000000000000000000000000000"
      },
      {
        "id": "1000",
        "startTime": "1643760796",
        "randomnessBN": "20421071",
        "randomness": "0x0000000000000000000000000000000000000000000000000000000000000000"
      },
      {
        "id": "1001",
        "startTime": "1643789596",
        "randomnessBN": "20426793",
        "randomness": "0x0000000000000000000000000000000000000000000000000000000000000000"
      },
      {
        "id": "1002",
        "startTime": "1643818396",
        "randomnessBN": "20432569",
        "randomness": "0x0000000000000000000000000000000000000000000000000000000000000000"
      },
      {
        "id": "1003",
        "startTime": "1643847196",
        "randomnessBN": "20438299",
        "randomness": "0x0000000000000000000000000000000000000000000000000000000000000000"
      }
    ]
  }
```

#### This example shows how to query an organization within a Garden <a href="#this-example-shows-how-to-query-an-organization-within-a-garden" id="this-example-shows-how-to-query-an-organization-within-a-garden"></a>

```
query Organizations(
  $first: Int!
  $skip: Int!
  $orderBy: String!
  $orderDirection: String!
) {
  organizations(
    first: $first
    where: { active: true }
    skip: $skip
    orderBy: $orderBy
    orderDirection: $orderDirection
  ) {
    id
    active
    createdAt
    proposalCount
    token {
      id
      symbol
      name
      decimals
    }
    wrappableToken {
      id
      symbol
      name
      decimals
    }
    honeyLiquidity
    supporterCount
    incentivisedPriceOracle
    unipool
  }
}
```

#### Result <a href="#result" id="result"></a>

```
{
  "data": {
    "organizations": [
      {
        "id": "0x129fc6300ea81a22c13c25f507cd2f9f902ca235",
        "createdAt": "1642661584",
        "config": {
          "id": "0x129fc6300ea81a22c13c25f507cd2f9f902ca235"
        },
        "token": {
          "id": "0xb2a02035ca4c046e2f9c8235b619ed1e6d630290"
        }
      },
      {
        "id": "0x316da8dab6c605681c07142f71ab6fd92a450cf2",
        "createdAt": "1648125547",
        "config": {
          "id": "0x316da8dab6c605681c07142f71ab6fd92a450cf2"
        },
        "token": {
          "id": "0xa5892b40056c77ef46ff20c21035366774bda0f5"
        }
      },
      {
        "id": "0x5fdaba692f7efc5d2ab372f84d6e0c17a16534c0",
        "createdAt": "1641156060",
        "config": {
          "id": "0x5fdaba692f7efc5d2ab372f84d6e0c17a16534c0"
        },
        "token": {
          "id": "0xe7b81d9408192fa7af47fdf051b5088e925ecac9"
        }
      },
      {
        "id": "0x7fba5b2fbbe327a0c5d2375cc260b76f021190ce",
        "createdAt": "1648150055",
        "config": {
          "id": "0x7fba5b2fbbe327a0c5d2375cc260b76f021190ce"
        },
        "token": {
          "id": "0xc550fc3ccdffe465ad36ed449befe1e18e5bd559"
        }
      }
    ],
    "configs": [
      {
        "id": "0x129fc6300ea81a22c13c25f507cd2f9f902ca235",
        "conviction": {
          "id": "0x7749884772a995168fff35565255052a7278a940"
        },
        "voting": {
          "id": "0x22b2610b98b01c5468d73a7783eba06ef2bf93d8-setting-0"
        }
      },
      {
        "id": "0x316da8dab6c605681c07142f71ab6fd92a450cf2",
        "conviction": {
          "id": "0xb9b5950d08b6bce61ca2a792acf574f550c2c4fc"
        },
        "voting": {
          "id": "0xe24aea8933bed0868d4ab864847bf9de65a76f20-setting-0"
        }
      },
      {
        "id": "0x5fdaba692f7efc5d2ab372f84d6e0c17a16534c0",
        "conviction": {
          "id": "0x5e759a5379e838ec45c022f0bce14f1ae7968b15"
        },
        "voting": {
          "id": "0x20c263c6cc44b97ee49f826dc004b17a9e3b4d25-setting-0"
        }
      },
      {
        "id": "0x7fba5b2fbbe327a0c5d2375cc260b76f021190ce",
        "conviction": null,
        "voting": {
          "id": "0x51945036a3e94dda6f4c6552a991b3a1c687dd6f-setting-0"
        }
      }
    ]
  }
}
```
