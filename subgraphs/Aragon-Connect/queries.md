# Querying Aragon

You can build your own queries using a [GraphQL Explorer](https://graphiql-online.com/graphiql) and enter your endpoint to limit the data to exactly what you need.

Each entity has a plural version and a singular version. When querying for a single record response (e.g. account), you will need to supply the id for the entity. When querying for a list of responses (e.g. accounts), you may add filters using the 'where' clause.

Below are some sample queries you can use to gather information from the Aragon Connect contracts.

## Examples

### The query below shows results from first 5 registry factories and 5 registries

```graphql
{
  registryFactories(first: 5) {
    id
    address
    registryCount
    registries {
      id
    }
  }
  registries(first: 5) {
    id
    address
    name
    node
  }
}
```

### Returns

```graphql
{
  "data": {
    "registryFactories": [
      {
        "id": "1",
        "address": "0xc36428063f69848d37bbb264087cf18ebec7c73e",
        "registryCount": 2,
        "registries": [
          {
            "id": "0x4fd8eec625fae26aabcb5283a184e2a9bbb4ccb4"
          },
          {
            "id": "0x6602c4a88febdfa3006d32da02929b585e373c4f"
          }
        ]
      }
    ],
    "registries": [
      {
        "id": "0x4fd8eec625fae26aabcb5283a184e2a9bbb4ccb4",
        "address": "0x4fd8eec625fae26aabcb5283a184e2a9bbb4ccb4",
        "name": "open.aragonpm.eth",
        "node": "0xbf6f73e6e925e595025f4fb0eec5a23cabd74a7a9b0d1f3e5bc88b44fa02e728"
      },
      {
        "id": "0x6602c4a88febdfa3006d32da02929b585e373c4f",
        "address": "0x6602c4a88febdfa3006d32da02929b585e373c4f",
        "name": "aragonpm.eth",
        "node": "0x9065c3e7f7b7ef1ef4e53d2d0b8e0cef02874ab020c1ece79d5f0d3d0111c0ba"
      }
    ]
  }
}
```

### The query below shows results from first 5 repos

```graphql
{
  repos(first: 5) {
    address
    appCount
    id
    name
  }
}
```

### Result

```graphql
{
  "data": {
    "repos": [
      {
        "address": "0x0542d65a6ff0e8d580f577b8795d80408dea25ae",
        "appCount": 0,
        "id": "0x0542d65a6ff0e8d580f577b8795d80408dea25ae",
        "name": "brightid-register"
      },
      {
        "address": "0x1f80483062779dff568241209cbd32cd9efbe8ae",
        "appCount": 0,
        "id": "0x1f80483062779dff568241209cbd32cd9efbe8ae",
        "name": "finance"
      },
      {
        "address": "0x36b2d126d80a3d446b891b9d7de4b329f8c1c7f5",
        "appCount": 0,
        "id": "0x36b2d126d80a3d446b891b9d7de4b329f8c1c7f5",
        "name": "agreement"
      },
      {
        "address": "0x3bbc3ff2c443dbacf3ea3b53e745d440352c7451",
        "appCount": 0,
        "id": "0x3bbc3ff2c443dbacf3ea3b53e745d440352c7451",
        "name": "reputation-template"
      },
      {
        "address": "0x3ea627b1d81366830203e0185c4874b506a25005",
        "appCount": 0,
        "id": "0x3ea627b1d81366830203e0185c4874b506a25005",
        "name": "token-manager"
      }
    ]
  }
}
```
