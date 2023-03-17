# Querying Celeste

You can build your own queries using a [GraphQL Explorer](https://graphiql-online.com/graphiql) and enter your endpoint to limit the data to exactly what you need.

Each entity has a plural version and a singular version. When querying for a single record response (e.g. account), you will need to supply the id for the entity. When querying for a list of responses (e.g. accounts), you may add filters using the ‘where’ clause.

Below are some sample queries you can use to gather information from the Celeste contracts.

### Examples <a href="#examples" id="examples"></a>

#### This query fetches aggredated data from Celest and obtains the first 5 CourtConfigs and CourtTerms information <a href="#this-query-fetches-aggredated-data-from-celest-and-obtains-the-first-5-courtconfigs-and-courtterms-i" id="this-query-fetches-aggredated-data-from-celest-and-obtains-the-first-5-courtconfigs-and-courtterms-i"></a>

```
{
  courtConfigs(first: 5) {
    id
    currentTerm
    termDuration
    feeToken {
      id
    }
  }
  courtTerms(first: 5) {
    id
    startTime
    randomnessBN
    randomness
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

#### This query fetches the first 5 appeals information <a href="#this-query-fetches-the-first-5-appeals-information" id="this-query-fetches-the-first-5-appeals-information"></a>

```
query MyQuery {
  appeals(first: 5) {
    id
    appealDeposit
    appealedRuling
    createdAt
  }
}
```

#### Result <a href="#result" id="result"></a>

```
{
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
