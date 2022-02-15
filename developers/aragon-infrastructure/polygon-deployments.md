# AragonOS Polygon Deployments

### ENS

| Name | Address                                    |
| ---- | ------------------------------------------ |
| ENS  | 0x7EdE100965B1E870d726cD480dD41F2af1Ca0130 |

### Aragon Bases

| Name                     | Address                                    |
| ------------------------ | ------------------------------------------ |
| Kernel                   | 0x0643Cd09CBE6c2a405efF4d165acD9206804623A |
| ACL                      | 0xF0e29CC532c198bdd09bF0c4e37c47DD68b32200 |
| EVMScriptRegistryFactory | 0x6A10a3012BFb0a59b01Aa9D1972b167103B04E22 |
| APMRegistry              | 0x0EA7ac6da7B5D69fBBD32038cE62A9dA1d096A8a |
| Repo                     | 0xC5Aa5bEF46697D537ef4aFcc04b91de166a899e4 |
| ENSSubdomainRegistrar    | 0x2c8C19E83CbCba9F942baf14666f0C7189F41E2c |

### Aragon Package Manager

| Name     | Address                                    |
| -------- | ------------------------------------------ |
| APM      | 0xEF680131a19179795797CD855661d174253E8801 |
| Open APM | 0xe4dC19D2d6dbE4eF45764e90Ad45B0DC4616aA7c |

### Factories

| Name               | Address                                    |
| ------------------ | ------------------------------------------ |
| DAOFactory         | 0xEe261Cf86cFf35d8657a4B5D4d1546B4d72c5314 |
| ENSFactory         | 0x9e1b16b6F25356a1f02F1391529Bd98Ba461905C |
| APMRegistryFactory | 0xdE63dBE180340918be86Eb8221b832Ad2E045081 |
| MiniMeTokenFactory | 0xcFed1594A5b1B612dC8199962461ceC148F14E68 |

### AragonID

| Name                   | Address                                    |
| ---------------------- | ------------------------------------------ |
| FIFSResolvingRegistrar | 0x7b9cd2d5eCFE44C8b64E01B93973491BBDAe879B |

### Deployment Script Output

```js
❯ npx hardhat deploy --network polygon
Nothing to compile
Creating Typechain artifacts in directory typechain for target ethers-v5
Successfully generated Typechain artifacts!
deploying "Kernel" (tx: 0x2b7c3492d278bdc8fec2d6668ff8ffb5b4ee0a8eb71681bb4af6b3b73ffecf5e)...: deployed at 0x0643Cd09CBE6c2a405efF4d165acD9206804623A with 2667669 gas
deploying "ACL" (tx: 0xc0d4e44e229622c30bb0edb30b952c279b9153c570bcd5bd360540ce84b26a3e)...: deployed at 0xF0e29CC532c198bdd09bF0c4e37c47DD68b32200 with 2622124 gas
deploying "EVMScriptRegistryFactory" (tx: 0x6719eca018de572f3708b81eb4d30b585511c7bf752dd58adcbe2a36a010e183)...: deployed at 0x6A10a3012BFb0a59b01Aa9D1972b167103B04E22 with 2534602 gas
deploying "DAOFactory" (tx: 0x8ecc4557f64b4eb542ffc024c9c133a52af78049d939944eeaf95a627fcd0814)...: deployed at 0xEe261Cf86cFf35d8657a4B5D4d1546B4d72c5314 with 996467 gas
deploying "APMRegistry" (tx: 0x80c22e1640df1bec4ba5701af61bd22a8faf4cc238fc9164d5372374ce958a38)...: deployed at 0x0EA7ac6da7B5D69fBBD32038cE62A9dA1d096A8a with 3314428 gas
deploying "Repo" (tx: 0x5c31ec398f04a049d2d21ddeca5a59c086a6f03c0c528e8a8f20f5b5668fbc14)...: deployed at 0xC5Aa5bEF46697D537ef4aFcc04b91de166a899e4 with 1704141 gas
deploying "ENSSubdomainRegistrar" (tx: 0x146740104ab6c5d2528ed113c52caf322b74db3bd9b23550f512bf21c0c0ae02)...: deployed at 0x2c8C19E83CbCba9F942baf14666f0C7189F41E2c with 1835993 gas
deploying "ENSFactory" (tx: 0x6678d323355d854b42f3ad7882a1566ed25fc1ba4f5b1650548495fda6e52e6f)...: deployed at 0x9e1b16b6F25356a1f02F1391529Bd98Ba461905C with 1821557 gas
ENS: 0x7EdE100965B1E870d726cD480dD41F2af1Ca0130
deploying "APMRegistryFactory" (tx: 0x22911308b88567ed68ceb52f555a878279b019673616a3533941c2f6dca4948d)...: deployed at 0xdE63dBE180340918be86Eb8221b832Ad2E045081 with 2210743 gas
Creating subdomain and assigning it to APMRegistryFactory
executing APMRegistryFactory.newAPM (tx: 0x944bcb95f4322edab20945f916505676f9f32784643c5df27d11e53c59a949b6) ...: performed with 4801955 gas
APM: 0xEF680131a19179795797CD855661d174253E8801
Create permission for root account on CREATE_NAME_ROLE
Creating open subdomain and assigning it to APMRegistryFactory
executing APMRegistryFactory.newAPM (tx: 0x40cbf0c19a34ac6aad59449c3a97b1db5426ba0ac68f344e051ac5f5a8f3ad76) ...: performed with 4801955 gas
Open APM: 0xe4dC19D2d6dbE4eF45764e90Ad45B0DC4616aA7c
Create permission for ANY_ENTITY on CREATE_REPO_ROLE
deploying "FIFSResolvingRegistrar" (tx: 0x33ee47623304bb213937ff95cb339b20f79cbeaccda027a9609da752d491206b)...: deployed at 0x7b9cd2d5eCFE44C8b64E01B93973491BBDAe879B with 423501 gas
Creating subdomain and assigning it to AragonID
Assigning owner name
executing FIFSResolvingRegistrar.register (tx: 0x468277558a4b0c940c4c48adcd654273bd37bd39c83e2a7028ff1c4bad677de6) ...: performed with 119042 gas
```

### Aragon apps

**🏗️ Agent**

```bash
➜ npx hardhat --network polygon publish major --skip-validation
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation contract
publish     | New implementation contract address: 0x1B35F10413859D25Cf63D27336eF0434acF113FD
publish     | Running app build script
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmSUuS2uJaSk3n6HGkGHNBDP3GPbYkwTPWMToe3pZvAVVq
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 
publish     |     status: prechecking
publish     |     name: polygon:agent.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry aragonpm.eth
publish     |
publish     |   App name:          agent.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0xB24b54FE5a3ADcB4cb3B27d31B6C7f7E9F6A73a7
publish     |   Contract address:  0x1B35F10413859D25Cf63D27336eF0434acF113FD
publish     |   ContentURI:        QmSUuS2uJaSk3n6HGkGHNBDP3GPbYkwTPWMToe3pZvAVVq
publish     |
publish     |   <https://ipfs.io/ipfs/QmSUuS2uJaSk3n6HGkGHNBDP3GPbYkwTPWMToe3pZvAVVq>
```

&#x20;**🏗️ Finance**

```bash
➜ npx hardhat --network polygon publish major
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x6645516FED458f900B5c89a095e0a6D099c6D529
publish     | Running app build script
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmTDd5bX3jkhSm5pwGwKbmmQ4pEGjrsEe9svk9TmQNttVJ
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 859a9893-9138-4c7a-856f-67b1a90aed5f
publish     |     status: prechecking
publish     |     name: polygon:finance.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry aragonpm.eth
publish     |
publish     |   App name:          finance.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0xB24b54FE5a3ADcB4cb3B27d31B6C7f7E9F6A73a7
publish     |   Contract address:  0x6645516FED458f900B5c89a095e0a6D099c6D529
publish     |   ContentURI:        QmTDd5bX3jkhSm5pwGwKbmmQ4pEGjrsEe9svk9TmQNttVJ
publish     |
publish     |   <https://ipfs.io/ipfs/QmTDd5bX3jkhSm5pwGwKbmmQ4pEGjrsEe9svk9TmQNttVJ>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x9239859127322d9488978916716644da1c6225ecfcf567d4223f6fa86516ef36
publish     |
publish     |   <https://explorer-mainnet.maticvigil.com/tx/0x9239859127322d9488978916716644da1c6225ecfcf567d4223f6fa86516ef36>
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  14531205
publish     |   Gas used:      960555
publish     |
```

&#x20;**🏗️ Token Manager**

```bash
➜ npx hardhat --network polygon publish major
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0xc271F2382ec150dE7536168F10C988766Eb0815b
publish     | Running app build script
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: Qmb4kqYbH7htBmc2uXMz5KZMPsTupnfYzvDUHKUxmRApjd
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 39cbf26e-5d50-4cb8-bbd0-edc720163443
publish     |     status: prechecking
publish     |     name: polygon:token-manager.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry aragonpm.eth
publish     |
publish     |   App name:          token-manager.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0xB24b54FE5a3ADcB4cb3B27d31B6C7f7E9F6A73a7
publish     |   Contract address:  0xc271F2382ec150dE7536168F10C988766Eb0815b
publish     |   ContentURI:        Qmb4kqYbH7htBmc2uXMz5KZMPsTupnfYzvDUHKUxmRApjd
publish     |
publish     |   <https://ipfs.io/ipfs/Qmb4kqYbH7htBmc2uXMz5KZMPsTupnfYzvDUHKUxmRApjd>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x6900fa9d138ddcbb5feb6f6f3e9bd6efe340e0e2fd78578e5120fefd2c2d218d
publish     |
publish     |   <https://explorer-mainnet.maticvigil.com/tx/0x6900fa9d138ddcbb5feb6f6f3e9bd6efe340e0e2fd78578e5120fefd2c2d218d>
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  14532086
publish     |   Gas used:      960627
publish     |
```

&#x20;**🏗️ Vault**

```bash
➜ npx hardhat --network polygon publish major
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x92f0155e2354461e8AD278dFA37ad7DA03fe9051
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: Qmc7TG1R9MQGWo4kqJ1XpqAAJ2ZDDvAHKpbMpfFwn2LsAa
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 47d70dbb-bbd5-4aa5-9747-5d6dabb88e03
publish     |     status: prechecking
publish     |     name: polygon:vault.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry aragonpm.eth
publish     |
publish     |   App name:          vault.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0xB24b54FE5a3ADcB4cb3B27d31B6C7f7E9F6A73a7
publish     |   Contract address:  0x92f0155e2354461e8AD278dFA37ad7DA03fe9051
publish     |   ContentURI:        Qmc7TG1R9MQGWo4kqJ1XpqAAJ2ZDDvAHKpbMpfFwn2LsAa
publish     |
publish     |   <https://ipfs.io/ipfs/Qmc7TG1R9MQGWo4kqJ1XpqAAJ2ZDDvAHKpbMpfFwn2LsAa>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x9118e5fd7ab5c06dcb3f39b3c0ea116bb53ce50d025e798ba8526fbe7fc552c6
publish     |
publish     |   <https://explorer-mainnet.maticvigil.com/tx/0x9118e5fd7ab5c06dcb3f39b3c0ea116bb53ce50d025e798ba8526fbe7fc552c6>
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  14531497
publish     |   Gas used:      960531
publish     |
```

**🏗️ Voting**

```bash
➜ npx hardhat --network polygon publish major
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0xD233d46dDEceEf8cC8679f281ee5892f94c2945c
publish     | Running app build script
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmQGrACNkH85iEUmQCQ3mANqKuWE1X8EjdPC1cyVNA9c6K
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 7e41c9cc-7051-40c3-853b-c13f0d58f796
publish     |     status: prechecking
publish     |     name: polygon:voting.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry aragonpm.eth
publish     |
publish     |   App name:          voting.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0xB24b54FE5a3ADcB4cb3B27d31B6C7f7E9F6A73a7
publish     |   Contract address:  0xD233d46dDEceEf8cC8679f281ee5892f94c2945c
publish     |   ContentURI:        QmQGrACNkH85iEUmQCQ3mANqKuWE1X8EjdPC1cyVNA9c6K
publish     |
publish     |   <https://ipfs.io/ipfs/QmQGrACNkH85iEUmQCQ3mANqKuWE1X8EjdPC1cyVNA9c6K>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x2a70c53458587e06f2fe6d33e4b9d8ba9b12372f967069e41280a73c2f9a9b1f
publish     |
publish     |   <https://explorer-mainnet.maticvigil.com/tx/0x2a70c53458587e06f2fe6d33e4b9d8ba9b12372f967069e41280a73c2f9a9b1f>
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  14531562
publish     |   Gas used:      960543
publish     |
```

**🏗️ Aggrements**

```jsx
❯ npx hardhat publish major --network polygon
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x7817a805598822985310b859c9E507a535b0c9D1
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmTZfMsvGHCGbuZHNR7PEcuQExADbNd3iXfdQszDU8GcW4
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 3f367a89-f216-4201-aa20-20ab6c3e8f06
publish     |     status: prechecking
publish     |     name: polygon:agreement.open.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry open.aragonpm.eth
publish     |
publish     |   App name:          agreement.open.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0x7817a805598822985310b859c9E507a535b0c9D1
publish     |   ContentURI:        QmTZfMsvGHCGbuZHNR7PEcuQExADbNd3iXfdQszDU8GcW4
publish     |
publish     |   [<https://ipfs.blossom.software/ipfs/QmTZfMsvGHCGbuZHNR7PEcuQExADbNd3iXfdQszDU8GcW4>](<https://ipfs.blossom.software/ipfs/QmTZfMsvGHCGbuZHNR7PEcuQExADbNd3iXfdQszDU8GcW4>)
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x63a7e8c2c855181441790fbe44b93543015645994e7f6cf44f9c3583d21c612d
publish     |
publish     |   [<https://explorer-mainnet.maticvigil.com/tx/0x63a7e8c2c855181441790fbe44b93543015645994e7f6cf44f9c3583d21c612d>](<https://explorer-mainnet.maticvigil.com/tx/0x63a7e8c2c855181441790fbe44b93543015645994e7f6cf44f9c3583d21c612d>)
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20610281
publish     |   Gas used:      850079
publish     |
```

**🏗️ Disputable Conviction Voting**

```jsx
❯ npx hardhat --network polygon publish major --skip-validation
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x696ee62e8684aac9c046B372dC7B4626CaD86335
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmTwnNj3QQS23zxbSmCTti7Xdn22A46M6KWbv9ArHy7WUd
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 32cb1ad9-1f57-4416-940b-3bd213d4b6e3
publish     |     status: prechecking
publish     |     name: polygon:disputable-conviction-voting.open.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry open.aragonpm.eth
publish     |
publish     |   App name:          disputable-conviction-voting.open.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0x696ee62e8684aac9c046B372dC7B4626CaD86335
publish     |   ContentURI:        QmTwnNj3QQS23zxbSmCTti7Xdn22A46M6KWbv9ArHy7WUd
publish     |
publish     |   <https://ipfs.io/ipfs/QmTwnNj3QQS23zxbSmCTti7Xdn22A46M6KWbv9ArHy7WUd>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0xb0a8063bc6819e7d800dd338e74d7d227b4a3815aaaf27bb2847c36e40d0d8c0
publish     |
publish     |   <https://polygonscan.com/tx/0xb0a8063bc6819e7d800dd338e74d7d227b4a3815aaaf27bb2847c36e40d0d8c0>
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20247168
publish     |   Gas used:      5247962
publish     |
```

**🏗️ Dynamic Issuance**

```jsx
❯ npx hardhat publish major --network polygon
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0xa8A99e55Bc2C033f0DAe577Acc50ef4dD399a495
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmRhDcSEeBc1YecJJFPyzC8SZSM2ef2xNThn9SMiRi1drh
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: bf5f32d2-6efc-4dd0-a2f9-9aacf113545e
publish     |     status: prechecking
publish     |     name: polygon:dynamic-issuance.open.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry open.aragonpm.eth
publish     |
publish     |   App name:          dynamic-issuance.open.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0xa8A99e55Bc2C033f0DAe577Acc50ef4dD399a495
publish     |   ContentURI:        QmRhDcSEeBc1YecJJFPyzC8SZSM2ef2xNThn9SMiRi1drh
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmRhDcSEeBc1YecJJFPyzC8SZSM2ef2xNThn9SMiRi1drh>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x5fda46bf1cb95216e030fb69c56a7d54d5cdf8ecec4cd9e7fd055004c60a2a0f
publish     |
publish     |   <https://explorer-mainnet.maticvigil.com/tx/0x5fda46bf1cb95216e030fb69c56a7d54d5cdf8ecec4cd9e7fd055004c60a2a0f>
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20667794
publish     |   Gas used:      850163
publish     |
```

```jsx
❯ npx hardhat publish major --network polygon
publish     | Applying version bump major, next version: 2.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0xA3740E43FD85AadDB2Fc2754ff0C03C134337219
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmbbrVLA92hgpMgXvCa5ZRkZ91pCic5crQeETakjaXAdNs
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 78f040f2-828b-4fd5-ba1f-99042b2549d6
publish     |     status: prechecking
publish     |     name: polygon:dynamic-issuance.open.aragonpm.eth@2.0.0
publish     |
publish     |   Publish new version 2.0.0 (major)
publish     |
publish     |   Contract address:  0xA3740E43FD85AadDB2Fc2754ff0C03C134337219
publish     |   ContentURI:        QmbbrVLA92hgpMgXvCa5ZRkZ91pCic5crQeETakjaXAdNs
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmbbrVLA92hgpMgXvCa5ZRkZ91pCic5crQeETakjaXAdNs>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0xe9730a0ff9f05708b40a2fd968602cb146a3c708635ca096eb6233e656780d0b
publish     |
publish     |   <https://explorer-mainnet.maticvigil.com/tx/0xe9730a0ff9f05708b40a2fd968602cb146a3c708635ca096eb6233e656780d0b>
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20668350
publish     |   Gas used:      245461
publish     |
```

**🏗️ Wrappable Hooked Token Manager**

```jsx
❯ npx hardhat publish major --network polygon
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x53e2B00C4b2e00FF1CB8B7Bee44927793cAE01F3
publish     | Running app build script
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmZLFvy6a6buaTnGkC4erjDhR3YqUUGcYLEG8grWvYrTj5
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 633e45e7-6aa8-4afd-944f-266c350240b9
publish     |     status: prechecking
publish     |     name: polygon:wrappable-hooked-token-manager.open.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry open.aragonpm.eth
publish     |
publish     |   App name:          wrappable-hooked-token-manager.open.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0x53e2B00C4b2e00FF1CB8B7Bee44927793cAE01F3
publish     |   ContentURI:        QmZLFvy6a6buaTnGkC4erjDhR3YqUUGcYLEG8grWvYrTj5
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmZLFvy6a6buaTnGkC4erjDhR3YqUUGcYLEG8grWvYrTj5>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0xf43a56daf9c16443b060255c49f0751ce8ec574d5ec24a7c1f0c7351c319d79f
publish     |
publish     |   <https://explorer-mainnet.maticvigil.com/tx/0xf43a56daf9c16443b060255c49f0751ce8ec574d5ec24a7c1f0c7351c319d79f>
publish     |
```

**🏗️ Voting Aggregator**

```jsx
❯ npx hardhat publish major --network polygon --skip-validation
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0xA767DAd3Bc47C59e15141e6F29609fe22f4b63aA
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmXHbt8ZVjuAzaVCy7343VKAQdnkQnxsVD1hHCrsT4o6rb
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 325fddf2-0fa1-45a3-8796-9433605e0d16
publish     |     status: prechecking
publish     |     name: polygon:vote-token-aggregator.open.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry open.aragonpm.eth
publish     |
publish     |   App name:          vote-token-aggregator.open.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0xA767DAd3Bc47C59e15141e6F29609fe22f4b63aA
publish     |   ContentURI:        QmXHbt8ZVjuAzaVCy7343VKAQdnkQnxsVD1hHCrsT4o6rb
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmXHbt8ZVjuAzaVCy7343VKAQdnkQnxsVD1hHCrsT4o6rb>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x28b8b55efb92c38aeb4894781039b943ff1489ced9f53fcce1099a6f11d356d8
publish     |
publish     |   <https://explorer-mainnet.maticvigil.com/tx/0x28b8b55efb92c38aeb4894781039b943ff1489ced9f53fcce1099a6f11d356d8>
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20681508
publish     |   Gas used:      850223
publish     |
```

&#x20;**🏗️ Disputable Voting**

```jsx
❯ npx hardhat publish major --network polygon --skip-validation --skip-app-build
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
Nothing to compile
publish     | New implementation contract address: 0x3E7F5a5dc128291171401fbEfaC648652C6E6180
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmQRYMRY5FeHkqQ9LpiPXC2jCYxYT5c3HFev6YS49ZDsqx
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 472526db-4b42-4f6d-b282-5d42b764e217
publish     |     status: prechecking
publish     |     name: polygon:disputable-voting.open.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry open.aragonpm.eth
publish     |
publish     |   App name:          disputable-voting.open.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0x5b0F8D8f47E3fDF7eE1c337AbCA19dBba98524e6
publish     |   Contract address:  0x3E7F5a5dc128291171401fbEfaC648652C6E6180
publish     |   ContentURI:        QmQRYMRY5FeHkqQ9LpiPXC2jCYxYT5c3HFev6YS49ZDsqx
publish     |
publish     |   <https://ipfs.blossom.software/ipfs/QmQRYMRY5FeHkqQ9LpiPXC2jCYxYT5c3HFev6YS49ZDsqx>
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x2d4b4c0d54587f9a9ce7ab3efe4ddebb9d5f083aba35a723216d47e451f8352f
publish     |
publish     |   <https://polygonscan.com/tx/0x2d4b4c0d54587f9a9ce7ab3efe4ddebb9d5f083aba35a723216d47e451f8352f>
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  20982709
publish     |   Gas used:      850175
publish     |
```
