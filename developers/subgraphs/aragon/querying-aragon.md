# Querying Aragon

You can build your own queries using a [GraphQL Explorer](https://graphiql-online.com/graphiql) and enter your endpoint to limit the data to exactly what you need.

Each entity has a plural version and a singular version. When querying for a single record response (e.g. account), you will need to supply the id for the entity. When querying for a list of responses (e.g. accounts), you may add filters using the ‘where’ clause.

Below are some sample queries you can use to gather information from the Aragon Agreement contracts.

### Examples <a href="#examples" id="examples"></a>

#### This query fetches the first 5 agreements and signers <a href="#this-query-fetches-the-first-5-agreements-and-signers" id="this-query-fetches-the-first-5-agreements-and-signers"></a>

```
{
  agreements(first: 5) {
    id
    dao
    stakingFactory
    currentVersion {
      id
    }
  }
  signers(first: 5) {
    id
    agreement {
      id
    }
    address
    actions {
      id
    }
  }
}
```

#### Returns <a href="#returns" id="returns"></a>

```
{
  "data": {
    "agreements": [
      {
        "id": "0x02dec3487c1b7dbadd7e716dbc80ca948bd53d96",
        "dao": "0x4cc26143871843ff1334d9bef3f93f0fd0ad3ebb",
        "stakingFactory": "0xe71331aef803baec606423b105e4d1c85f012c00",
        "currentVersion": {
          "id": "0x02dec3487c1b7dbadd7e716dbc80ca948bd53d96-version-1"
        }
      },
      {
        "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8",
        "dao": "0x6d986e213d0d66456a8d22841f29d022c1d95120",
        "stakingFactory": "0xe71331aef803baec606423b105e4d1c85f012c00",
        "currentVersion": {
          "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8-version-1"
        }
      },
      {
        "id": "0x09aaaf8cea7f56f14cdedb46718f05bb8c929175",
        "dao": "0xb3f3da0080a8811d887531ca4c0dbfe3490bd1a1",
        "stakingFactory": "0xe71331aef803baec606423b105e4d1c85f012c00",
        "currentVersion": {
          "id": "0x09aaaf8cea7f56f14cdedb46718f05bb8c929175-version-1"
        }
      },
      {
        "id": "0x0afb27d68580e9169cdfc192563f2d8912449586",
        "dao": "0x919c45abdd2025d115b09392dc151b77586aa3f1",
        "stakingFactory": "0xe71331aef803baec606423b105e4d1c85f012c00",
        "currentVersion": {
          "id": "0x0afb27d68580e9169cdfc192563f2d8912449586-version-1"
        }
      },
      {
        "id": "0x0f2239cdba335d2c51795e0cd43fb681b305a8d2",
        "dao": "0x2050eabe84409e480ad1062001fdb6dfbc836192",
        "stakingFactory": "0xe71331aef803baec606423b105e4d1c85f012c00",
        "currentVersion": {
          "id": "0x0f2239cdba335d2c51795e0cd43fb681b305a8d2-version-1"
        }
      }
    ],
    "signers": [
      {
        "id": "0x02dec3487c1b7dbadd7e716dbc80ca948bd53d96-signer-0x5f672d71399d8cdba64f596394b4f4381247e025",
        "agreement": {
          "id": "0x02dec3487c1b7dbadd7e716dbc80ca948bd53d96"
        },
        "address": "0x5f672d71399d8cdba64f596394b4f4381247e025",
        "actions": []
      },
      {
        "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8-signer-0x2c2fb1006b3d887330bd5fda14ed1f53e1e1c182",
        "agreement": {
          "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8"
        },
        "address": "0x2c2fb1006b3d887330bd5fda14ed1f53e1e1c182",
        "actions": []
      },
      {
        "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8-signer-0x3ebea5e6a6b41f151cd3da67e2f2c74dc577749f",
        "agreement": {
          "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8"
        },
        "address": "0x3ebea5e6a6b41f151cd3da67e2f2c74dc577749f",
        "actions": []
      },
      {
        "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8-signer-0x44cf9cc59bef89c316f633639bc852b33bc3b5df",
        "agreement": {
          "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8"
        },
        "address": "0x44cf9cc59bef89c316f633639bc852b33bc3b5df",
        "actions": []
      },
      {
        "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8-signer-0x809c9f8dd8ca93a41c3adca4972fa234c28f7714",
        "agreement": {
          "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8"
        },
        "address": "0x809c9f8dd8ca93a41c3adca4972fa234c28f7714",
        "actions": []
      }
    ]
  }
}
```

**This query fetches the first 5 collateral requirements with duration and symbol of token**

```
{
  collateralRequirements(first: 5) {
    challengeAmount
    challengeDuration
    id
    token {
      symbol
    }
  }
}
```

**Result**

```
{
  "data": {
    "collateralRequirements": [
      {
        "challengeAmount": "10000000000000000000000",
        "challengeDuration": "604800",
        "id": "0x02dec3487c1b7dbadd7e716dbc80ca948bd53d96-disputable-0x33a91b955764d4beb70f91d53cb7e3efc3c2fbf4-collateral-requirement-1",
        "token": {
          "symbol": "DRGIV3"
        }
      },
      {
        "challengeAmount": "10000000000000000000000",
        "challengeDuration": "604800",
        "id": "0x02dec3487c1b7dbadd7e716dbc80ca948bd53d96-disputable-0x539e4b7756bb2b6d405a897b134e4d2563697402-collateral-requirement-1",
        "token": {
          "symbol": "DRGIV3"
        }
      },
      {
        "challengeAmount": "100000000000000000",
        "challengeDuration": "259200",
        "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8-disputable-0x4e20482124aab5fc96d7f1abc209ea23ba325002-collateral-requirement-1",
        "token": {
          "symbol": "gCRC"
        }
      },
      {
        "challengeAmount": "100000000000000000",
        "challengeDuration": "259200",
        "id": "0x07c882b746d9ef16c56ac3dbf0d6b720f57344b8-disputable-0x5dd85d7f3cca8efbce982f86306b2ac1df885bdf-collateral-requirement-1",
        "token": {
          "symbol": "gCRC"
        }
      },
      {
        "challengeAmount": "10000000000000000000000",
        "challengeDuration": "604800",
        "id": "0x09aaaf8cea7f56f14cdedb46718f05bb8c929175-disputable-0x9ece49cc91cf0c272f5665a819612c694a18b54a-collateral-requirement-1",
        "token": {
          "symbol": "DRGIV2"
        }
      }
    ]
  }
}
```
