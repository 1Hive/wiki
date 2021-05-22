# Polygon deployments

### Aragon base contracts

```text
"Kernel" at 0x47c980A62bA89F738A668ED1709Ca5fef2384F21
"ACL" at 0xe8BB56B204950b0E06188AFf22c0665E71ED8312
"EVMScriptRegistryFactory" at 0xd066b4136E3318A9a054d04AA90e7B0fc0ae03cb
"DAOFactory" at 0xfCBF0FCAf5851dD9221f2C0FefdFF7f7A14b478a
"APMRegistry" at 0x749C45B5A3842Cc758d3c7CAb3Fb6354De371aC5
"Repo" at 0x6099327dd7b8BefcBd607453C9029CbE148845a7
"ENSSubdomainRegistrar" at 0xDE49D96d85D6BF630604EE4812b2511bD3286Fb5
"ENSFactory" at 0xF6D7B706B53e1D1Dd70DE015f2a169bd0501bdf1
executing ENSFactory.newENS (tx: 0x7727385ce9896eb47ab3409c0e5f5c20b71aeedae3d4144a044c2c41c81c8781) ...: performed with 1565278 gas
ENS: 0x4E065c622d584Fbe5D9078C3081840155FA69581
"APMRegistryFactory" at 0xb8c830ACebD05537dDDbc45F568aADc5a7cd952D

Creating subdomain and assigning it to APMRegistryFactor
executing APMRegistryFactory.newAPM (tx: 0xd8f5100e0f5dd914293b3140e15916d76b9110a457700cb160562a13e5346d73) ...: performed with 5847155 gas
APM: 0x21083376cE8c426008663701d14976F0eb8B4043

Create permission for root account on CREATE_NAME_ROLE
Creating open subdomain and assigning it to APMRegistryFactory
executing APMRegistryFactory.newAPM (tx: 0x9e3b6a309b658cdd695bfae91c06decb8c61843cfab7e8b112d35338218bd294) ...: performed with 5847155 gas
Open APM: 0xc00E44fBCeDf652e52E4C86B89a7812dE9b0E9f8

"FIFSResolvingRegistrar" (AragonID) at 0x3d5e84D0708744f0Af7dd1AD28df6E5FB92473C0 with 419627 gas
Creating subdomain aragonid.eth and assigning it to AragonID
```

### Aragon shared contracts

```text
"BaseTemplate" at 0x8C50E11514E9aA69543F0b369c70c1BED90c78A8
"MiniMeTokenFactory" at 0x64cDB6caa54Db0703078D6C693cf87Bc16EA777D
```

### Aragon apps

#### Agent

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
publish     |   https://ipfs.io/ipfs/QmSUuS2uJaSk3n6HGkGHNBDP3GPbYkwTPWMToe3pZvAVVq
```

#### Agreements

```bash
➜ npx hardhat --network polygon publish major
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0x41B0039fcC760B8899b3D11e954A7A7B5dfC9E4c
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmekfVPGoJVb2voBY2D4j6fJKWmMcGcuyWt5N588amATYe
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: 91c62f55-2f29-4fd2-a4db-81f981c3de65
publish     |     status: prechecking
publish     |     name: polygon:agreement.open.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry open.aragonpm.eth
publish     |
publish     |   App name:          agreement.open.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0xB24b54FE5a3ADcB4cb3B27d31B6C7f7E9F6A73a7
publish     |   Contract address:  0x41B0039fcC760B8899b3D11e954A7A7B5dfC9E4c
publish     |   ContentURI:        QmekfVPGoJVb2voBY2D4j6fJKWmMcGcuyWt5N588amATYe
publish     |
publish     |   https://ipfs.io/ipfs/QmekfVPGoJVb2voBY2D4j6fJKWmMcGcuyWt5N588amATYe
publish     |
```

#### Finance

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
publish     |   https://ipfs.io/ipfs/QmTDd5bX3jkhSm5pwGwKbmmQ4pEGjrsEe9svk9TmQNttVJ
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x9239859127322d9488978916716644da1c6225ecfcf567d4223f6fa86516ef36
publish     |
publish     |   https://explorer-mainnet.maticvigil.com/tx/0x9239859127322d9488978916716644da1c6225ecfcf567d4223f6fa86516ef36
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  14531205
publish     |   Gas used:      960555
publish     |
```

#### Token Manager

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
publish     |   https://ipfs.io/ipfs/Qmb4kqYbH7htBmc2uXMz5KZMPsTupnfYzvDUHKUxmRApjd
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x6900fa9d138ddcbb5feb6f6f3e9bd6efe340e0e2fd78578e5120fefd2c2d218d
publish     |
publish     |   https://explorer-mainnet.maticvigil.com/tx/0x6900fa9d138ddcbb5feb6f6f3e9bd6efe340e0e2fd78578e5120fefd2c2d218d
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  14532086
publish     |   Gas used:      960627
publish     |
```

#### Vault

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
publish     |   https://ipfs.io/ipfs/Qmc7TG1R9MQGWo4kqJ1XpqAAJ2ZDDvAHKpbMpfFwn2LsAa
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x9118e5fd7ab5c06dcb3f39b3c0ea116bb53ce50d025e798ba8526fbe7fc552c6
publish     |
publish     |   https://explorer-mainnet.maticvigil.com/tx/0x9118e5fd7ab5c06dcb3f39b3c0ea116bb53ce50d025e798ba8526fbe7fc552c6
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  14531497
publish     |   Gas used:      960531
publish     |
```

#### Voting

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
publish     |   https://ipfs.io/ipfs/QmQGrACNkH85iEUmQCQ3mANqKuWE1X8EjdPC1cyVNA9c6K
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0x2a70c53458587e06f2fe6d33e4b9d8ba9b12372f967069e41280a73c2f9a9b1f
publish     |
publish     |   https://explorer-mainnet.maticvigil.com/tx/0x2a70c53458587e06f2fe6d33e4b9d8ba9b12372f967069e41280a73c2f9a9b1f
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  14531562
publish     |   Gas used:      960543
publish     |
```

#### Voting Disputable

The front-end was not building and the app was published without it.

```bash
❯ npx hardhat publish major --network polygon --skip-validation
publish     | Applying version bump major, next version: 1.0.0
publish     | Deploying new implementation or reusing last deployment if no changes.
publish     | New implementation contract address: 0xd5D602A81098b33E3086407c3AfFAcd88b15B933
publish     | Generating Aragon app artifacts
publish     | Uploading release assets to IPFS...
publish     | Release assets uploaded to IPFS: QmUFq3ASFTYpGFea5fVFvUqjfz6xtmUrDc8qCkHt7ktQ4K
publish     | Pinning content to pinata...
publish     | Content pinned:
publish     |     id: fa576746-610a-402d-b0bc-fa1ae5fdcd4a
publish     |     status: prechecking
publish     |     name: polygon:disputable-voting.open.aragonpm.eth@1.0.0
publish     |
publish     |   Deploy new repo to registry open.aragonpm.eth
publish     |
publish     |   App name:          disputable-voting.open.aragonpm.eth
publish     |   Initial version:   1.0.0
publish     |   Manager address:   0xB24b54FE5a3ADcB4cb3B27d31B6C7f7E9F6A73a7
publish     |   Contract address:  0xd5D602A81098b33E3086407c3AfFAcd88b15B933
publish     |   ContentURI:        QmUFq3ASFTYpGFea5fVFvUqjfz6xtmUrDc8qCkHt7ktQ4K
publish     |
publish     |   https://ipfs.io/ipfs/QmUFq3ASFTYpGFea5fVFvUqjfz6xtmUrDc8qCkHt7ktQ4K
publish     |
publish     |
publish     |   Tx sent
publish     |
publish     |   Tx hash:  0xa789dfd8348e37576e66807cd36381a2f89a4b4db89597b113456c18294fa194
publish     |
publish     |   https://explorer-mainnet.maticvigil.com/tx/0xa789dfd8348e37576e66807cd36381a2f89a4b4db89597b113456c18294fa194
publish     |
publish     |
publish     |   Tx mined
publish     |
publish     |   Status:        Success
publish     |   Block number:  14710354
publish     |   Gas used:      960675
publish     |
```

