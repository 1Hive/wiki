# Mumbai

### ENS

| Name | Address                                    |
| ---- | ------------------------------------------ |
| ENS  | 0xB1576a9bE5EC445368740161174f3Dd1034fF8be |

### Aragon Bases

| Name                     | Address                                    |
| ------------------------ | ------------------------------------------ |
| Kernel                   | 0xD1cf4cf213ff1deC94b4879356ab481B47369dfD |
| ACL                      | 0x53F03714e7D2BBF6498d9CB2b26854dAa2Ecc7a7 |
| EVMScriptRegistryFactory | 0x99dfA87eA183E0e21f977255F768Ae453FFeba64 |
| APMRegistry              | 0x9d51Fd641e420692e981DdF4345b1917ee16E880 |
| Repo                     | 0x0643Cd09CBE6c2a405efF4d165acD9206804623A |
| ENSSubdomainRegistrar    | 0xF0e29CC532c198bdd09bF0c4e37c47DD68b32200 |

### Aragon Package Manager

| Name     | Address                                    |
| -------- | ------------------------------------------ |
| APM      | 0xE5Ff665BD031bc044F47ba5611F5450d69B733F4 |
| Open APM | 0x6C66Ec1437DaDc26070B731ccE0086F9Aef41b4a |

### Factories

| Name               | Address                                    |
| ------------------ | ------------------------------------------ |
| DAOFactory         | 0xE97999F411333E3B712104aa04fc06b149BD12eA |
| ENSFactory         | 0x6A10a3012BFb0a59b01Aa9D1972b167103B04E22 |
| APMRegistryFactory | 0x0EA7ac6da7B5D69fBBD32038cE62A9dA1d096A8a |
| MiniMeFactory      | 0x14E1326445077E2E170eb48785a849e30D502994 |

### AragonID

| Name                   | Address                                    |
| ---------------------- | ------------------------------------------ |
| FIFSResolvingRegistrar | 0xb7E098cB86b120363A935730970A3758861ba458 |

### Deployment Script Output

```js
❯ npx hardhat deploy --network mumbai
Nothing to compile
Creating Typechain artifacts in directory typechain for target ethers-v5
Successfully generated Typechain artifacts!
deploying "Kernel" (tx: 0xc29bdf7bdbcc2089e17f89b8578270f40cffa5f0be3644eeb605ec20545f0de5)...: deployed at 0xD1cf4cf213ff1deC94b4879356ab481B47369dfD with 2667669 gas
deploying "ACL" (tx: 0x3ed544b40fc303fa27075a0caaafc676b614acb232eb6ff290933385350a9dbe)...: deployed at 0x53F03714e7D2BBF6498d9CB2b26854dAa2Ecc7a7 with 2622124 gas
deploying "EVMScriptRegistryFactory" (tx: 0x7b42ce14bc39b51cff7dac9e3a71d8f0e2bf8d2787c71b10880d50aca28c6c17)...: deployed at 0x99dfA87eA183E0e21f977255F768Ae453FFeba64 with 2534602 gas
deploying "DAOFactory" (tx: 0x5b5391d4d4e38510fcb8acf38bf2300471e334c48971deba1fac03894a12463e)...: deployed at 0xE97999F411333E3B712104aa04fc06b149BD12eA with 996479 gas
deploying "APMRegistry" (tx: 0xf189e267d12ceafe17c74de479dcb8de1b4554ddb79933b701b1c2f3483f78d8)...: deployed at 0x9d51Fd641e420692e981DdF4345b1917ee16E880 with 3314428 gas
deploying "Repo" (tx: 0x98c04df924d57f4e30a9f2731a31cb0e7f967233750d55d9290496225f2f47e4)...: deployed at 0x0643Cd09CBE6c2a405efF4d165acD9206804623A with 1704141 gas
deploying "ENSSubdomainRegistrar" (tx: 0x2a6ab252dd166080b911b9146616bb61db10ce442a8c6a0122f80d2f09e64eac)...: deployed at 0xF0e29CC532c198bdd09bF0c4e37c47DD68b32200 with 1835993 gas
deploying "ENSFactory" (tx: 0x7a36e79109b57c039a6adbbc7d11128f3719b3219c8da5fc1981939326251b14)...: deployed at 0x6A10a3012BFb0a59b01Aa9D1972b167103B04E22 with 1821557 gas
executing ENSFactory.newENS (tx: 0x7316ad5bebe836e94a9d8be06c3c4d6152870e6f688b67337dfe33d2f822973b) ...: performed with 1556978 gas
ENS: 0xB1576a9bE5EC445368740161174f3Dd1034fF8be
Creating subdomain and assigning it to APMRegistryFactory
APM: 0xE5Ff665BD031bc044F47ba5611F5450d69B733F4
Create permission for root account on CREATE_NAME_ROLE
Creating open subdomain and assigning it to APMRegistryFactory
executing APMRegistryFactory.newAPM (tx: 0x39edfd9b41fb9fde4fa660f4b5e496331da610dce9c0f3530a47ee6089f3aa4f) ...: performed with 4801955 gas
Open APM: 0x6C66Ec1437DaDc26070B731ccE0086F9Aef41b4a
Create permission for ANY_ENTITY on CREATE_REPO_ROLE
deploying "FIFSResolvingRegistrar" (tx: 0x78279dd3f39507eda75874f9ebeaed53b6ef8c907dcad631209015c7e3cfb7b0)...: deployed at 0xb7E098cB86b120363A935730970A3758861ba458 with 423489 gas
Creating subdomain and assigning it to AragonID
Assigning owner name
executing FIFSResolvingRegistrar.register (tx: 0x845575f7d2fe15b09569692774cc2705b15989b24ee3a00155ada0e1d642f869) ...: performed with 119042 gas
```

### Aragon apps

**🏗️ Agent**

```jsx
❯ npx hardhat --network mumbai publish major --skip-validation
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x1B35F10413859D25Cf63D27336eF0434acF113FD
publish     | Running app build script
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmSUuS2uJaSk3n6HGkGHNBDP3GPbYkwTPWMToe3pZvAVVq
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 1e6d6f68-23fa-4f8e-b472-2892c5be364e
publish     |     status: prechecking
publish     |     name: mumbai:agent.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry aragonpm.eth
publish     |
publish     |   App name:          agent.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0x1B35F10413859D25Cf63D27336eF0434acF113FD
publish     |   ContentURI:        QmSUuS2uJaSk3n6HGkGHNBDP3GPbYkwTPWMToe3pZvAVVq
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmSUuS2uJaSk3n6HGkGHNBDP3GPbYkwTPWMToe3pZvAVVq>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x32a8a1bc668590c3dd31f3026186e1170b48a501ce54f0e872e3502ee527d164
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20141629
publish     |   Gas used:      850031
publish     |
```

**🏗️ Agreement**

```jsx
❯ npx hardhat --network mumbai publish major
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x41B0039fcC760B8899b3D11e954A7A7B5dfC9E4c
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmekfVPGoJVb2voBY2D4j6fJKWmMcGcuyWt5N588amATYe
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: a0f9c516-e93b-45dc-8dd3-68153d60302c
publish     |     status: prechecking
publish     |     name: mumbai:agreement.open.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry open.aragonpm.eth
publish     |
publish     |   App name:          agreement.open.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0x41B0039fcC760B8899b3D11e954A7A7B5dfC9E4c
publish     |   ContentURI:        QmekfVPGoJVb2voBY2D4j6fJKWmMcGcuyWt5N588amATYe
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmekfVPGoJVb2voBY2D4j6fJKWmMcGcuyWt5N588amATYe>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0xcc22c297b95aaf8595ac11d2f2a6c64cf9906ef303ff1d1ea3b75fe13a2bcfec
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20141843
publish     |   Gas used:      850079
publish     |
```

```jsx
❯ npx hardhat --network mumbai publish patch
publish     | Applying version bump patch, next version: 1.0.1
publish     | Reusing previous version contract address: 0x41B0039fcC760B8899b3D11e954A7A7B5dfC9E4c
publish     | Resolving Aragon artifacts from Aragon Package Manager
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmPC2QfTJ8Q3wcNUPW1aJJfTjtpvbbcUgaV243MGJK58hB
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: ca5bb4b2-b279-4de1-bb53-c979d5c26daa
publish     |     status: prechecking
publish     |     name: mumbai:agreement.open.aragonpm.eth@1.0.1
publish     |
publish     |   Publish new version 1.0.1 (patch)
publish     |
publish     |   Contract address:  0x41B0039fcC760B8899b3D11e954A7A7B5dfC9E4c
publish     |   ContentURI:        QmPC2QfTJ8Q3wcNUPW1aJJfTjtpvbbcUgaV243MGJK58hB
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmPC2QfTJ8Q3wcNUPW1aJJfTjtpvbbcUgaV243MGJK58hB>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x965425a95dee59c31c0391907894d9dcd41dc1e3ef9880daca67aaaae464fa6d
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20142168
publish     |   Gas used:      228317
publish     |
```

```bash
❯ npx hardhat publish major --network mumbai
publish     | Applying version bump major, next version: 2.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x7817a805598822985310b859c9E507a535b0c9D1
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmTZfMsvGHCGbuZHNR7PEcuQExADbNd3iXfdQszDU8GcW4
publish     |
publish     |   Publish new version 2.0.0 (major)
publish     |
publish     |   Contract address:  0x7817a805598822985310b859c9E507a535b0c9D1
publish     |   ContentURI:        QmTZfMsvGHCGbuZHNR7PEcuQExADbNd3iXfdQszDU8GcW4
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmTZfMsvGHCGbuZHNR7PEcuQExADbNd3iXfdQszDU8GcW4>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x6bc41dac8c9f5a36dae3cfd19c65f6adb3c4c9b5c86eca89a04b5aa8b88053a2
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20182939
publish     |   Gas used:      245461
publish     |
```

**🏗️ Finance**

```jsx
❯ npx hardhat --network mumbai publish major
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x6645516FED458f900B5c89a095e0a6D099c6D529
publish     | Running app build script
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmaqE17szGN38uQMgCVCmRMP7bVL63zCi1eHoV3RR6gvfE
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 5efda56a-ee00-4b95-93be-56a77edda98b
publish     |     status: prechecking
publish     |     name: mumbai:finance.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry aragonpm.eth
publish     |
publish     |   App name:          finance.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0x6645516FED458f900B5c89a095e0a6D099c6D529
publish     |   ContentURI:        QmaqE17szGN38uQMgCVCmRMP7bVL63zCi1eHoV3RR6gvfE
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmaqE17szGN38uQMgCVCmRMP7bVL63zCi1eHoV3RR6gvfE>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x2422504aa5336a1e85194a11edb64cd0036f0b4c8f1d1cc1390416dc9e3e2e63
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20141970
publish     |   Gas used:      850055
publish     |
```

**🏗️ Token Manager**

```jsx
❯ npx hardhat --network mumbai publish major
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0xc271F2382ec150dE7536168F10C988766Eb0815b
publish     | Running app build script
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmWQ1HM79TuWN1vdsQnSTuDDbNYcjLEDt9ydfisSUH4A1Q
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: c54b1c9a-5c14-43d9-ba2f-5a1789fccf92
publish     |     status: prechecking
publish     |     name: mumbai:token-manager.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry aragonpm.eth
publish     |
publish     |   App name:          token-manager.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0xc271F2382ec150dE7536168F10C988766Eb0815b
publish     |   ContentURI:        QmWQ1HM79TuWN1vdsQnSTuDDbNYcjLEDt9ydfisSUH4A1Q
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmWQ1HM79TuWN1vdsQnSTuDDbNYcjLEDt9ydfisSUH4A1Q>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0xf152db66e76e3851a833a17381e3662ca538d8a30a471748c10e4472bddd15cd
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20142085
publish     |   Gas used:      850127
publish     |
```

**🏗️ Vault**

```jsx
❯ npx hardhat --network mumbai publish major
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x92f0155e2354461e8AD278dFA37ad7DA03fe9051
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: Qmc7TG1R9MQGWo4kqJ1XpqAAJ2ZDDvAHKpbMpfFwn2LsAa
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 18a1497f-ac51-47f5-9dd0-108b1bb685eb
publish     |     status: prechecking
publish     |     name: mumbai:vault.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry aragonpm.eth
publish     |
publish     |   App name:          vault.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0x92f0155e2354461e8AD278dFA37ad7DA03fe9051
publish     |   ContentURI:        Qmc7TG1R9MQGWo4kqJ1XpqAAJ2ZDDvAHKpbMpfFwn2LsAa
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/Qmc7TG1R9MQGWo4kqJ1XpqAAJ2ZDDvAHKpbMpfFwn2LsAa>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0xfa278f6100312c9baafba3baecea5a7c08b6bf91a5d5d81f68cda7c5eb23b2a8
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20142251
publish     |   Gas used:      850031
publish     |
```

**🏗️ Voting**

```jsx
❯ npx hardhat --network mumbai publish major
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0xD233d46dDEceEf8cC8679f281ee5892f94c2945c
publish     | Running app build script
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmcQzRkMrQ6B3pimw6dqYszeQitxz7yrTzxuCRXLsJLeDG
publish     |
publish     |   Deploy new repo to registry aragonpm.eth
publish     |
publish     |   App name:          voting.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0xD233d46dDEceEf8cC8679f281ee5892f94c2945c
publish     |   ContentURI:        QmcQzRkMrQ6B3pimw6dqYszeQitxz7yrTzxuCRXLsJLeDG
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmcQzRkMrQ6B3pimw6dqYszeQitxz7yrTzxuCRXLsJLeDG>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x9121224a9cda90618f5c446fca556ee2302ced61251f51233248a30e2500bfb5
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20142338
publish     |   Gas used:      850043
publish     |
```



