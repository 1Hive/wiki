# xDai

### ENS registry

```
Deploying ENSFactory...
=========
# ENSFactory:
Address: 0x646e555928ebc2752730aa344ee959ce846e75ab
Transaction hash: 0xa15aadf122d45c74656a1683db6aeee6b793fe42883344215581866f5ff72d5d
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-05-24T05:55:24.617Z
=========
====================
Deployed ENS: 0xaafca6b0c89521752e559650206d7c925fd0e530
=========
Deployed PublicResolver: 0x4De3793A50474304a61276AD927E30eeD35F0edE
```

### Aragon base contracts

```
Deploying APM...
Owner: 0x625236038836cecc532664915bd0399647e7826b
ENS: 0xaafca6b0c89521752e559650206d7c925fd0e530
TLD: eth (0x93cdeb708b7545dc668eb9280176169d1c33cfd8ed6f04690a0bcc88a93fc4ae)
Label: aragonpm (0x1542111b4698ac085139692eae7c6efb632a4ae2779f8686da94511ebbbff594)
=========
Deploying APM bases...
=========
# APMRegistry:
Address: 0x3c9fdcf51c3447f629fc61f6aaaf2ac3ea852040
Transaction hash: 0x0f1f4a29f4968a00c563042f7e36c3b3134b911aacf342fbc142b96f10ed7df9
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-05-24T05:55:24.662Z
=========
=========
# Repo:
Address: 0xfc9c308608d2bf56faaad456b574e07c5cef08bf
Transaction hash: 0x1f568e9a87b970259c1e2a0fca8593240ad0f8b150b8d6abe97da3456bc9e926
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-05-24T05:55:24.669Z
=========
=========
# ENSSubdomainRegistrar:
Address: 0xfab761b1630c8829761e6952b06af50e98c495a3
Transaction hash: 0xe74d536a544d0d0b7e2d15f76176dce87666ec647c240756748fc70e6895af73
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-05-24T05:55:24.657Z
=========
Deploying DAOFactory with EVMScripts...
Deployed Kernel: 0x336ebb4def4da4fad6936874b8c952e800024653
Deployed ACL: 0x4499948d089330df05795b08aa23a964027b9cd8
Deployed EVMScriptRegistryFactory: 0xeac7fbf38a6e1b7e38bd11cea16850cded67817e
Deployed DAOFactory: 0x4037f97fcc94287257e50bd14c7da9cb4df18250
Deploying APMRegistryFactory...
=========
# APMRegistryFactory:
Address: 0x812672c031210b439a5befc8f397d639e97e3738
Transaction hash: 0xbbbefcc639e682cd2f1de1594b03605efddddc0ae3a912a66a2a001a55a8444f
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-05-24T05:55:24.699Z
=========
Assigning ENS name (aragonpm.eth) to factory...
Creating subdomain and assigning it to APMRegistryFactory
Deploying APM...
=========
# APM:
Address: 0xb10ee07356b175a3bec591745296ed93d2f857f3 
Transaction hash: 0x7999fa7d7ee841eccc88a6a661b32770ac6f1022ef29850eb620225adae541c7
=========
Managing permissions...
assign create name role permission to owner
=========
TLD: aragonpm.eth (0x9065c3e7f7b7ef1ef4e53d2d0b8e0cef02874ab020c1ece79d5f0d3d0111c0ba)
Open Label: open (0x99f30275ab70dd1890c0789c4570632b6f0b0284d11c2d9e587d0368f7027018)
Hatch Label: 1hive (0xbef57f662870bc4f372075f07bd453a9cfc5c22a370b5bf41fdb74c839229f3e)
=========
Assigning ENS name (open.aragonpm.eth) and (1hive.aragonpm.eth) to factory...
=========
Deploying Open APM...
=========
=========
# Open APM:
Address: 0xac9ca92d16e8bc0505eda84573d614ffecd8a293
Transaction hash: 0xe50ab2ef530076fee65fa3dd0982c36feeaa908e0a0ee9d0cedf2cfb39f67482
=========
=========
Deploying 1Hive APM...
=========
# 1Hive APM:
Address: 0x8ee864e13e4754713db2150f2b584180ee479fa8
Transaction hash: 0xc6634b304ddef662b3299fbce97022d7053a84f98801e16b6c0a13a954236b9e
=========
aragonpm.eth registry DAO: 0xF80d62c74aaEf8F97d1fba4A6ec15a63E3cD4e94
=========
open.aragonpm.eth registry DAO: 0x792281C15227F16BbeC04425b60c5B9B678A1c94
```

### AragonID

```
Deploying AragonID with ENS: 0xaafca6b0c89521752e559650206d7c925fd0e530 and owner: 0x625236038836CecC532664915BD0399647E7826b
=========
# FIFSResolvingRegistrar:
Address: 0x0b3b17f9705783bb51ae8272f3245d6414229b36
Transaction hash: 0xa2099d87ee32c610e6cd8037b7b833bd890e84be16a7af5c43f2407e040991d8
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-05-24T05:55:24.624Z
=========
assigning ENS name to AragonID
Creating subdomain and assigning it to AragonID
assigning owner name
===========
Deployed AragonID: 0x0b3b17f9705783bb51ae8272f3245d6414229b36
===========
```

### Minime factory

```
=========
Deploying Minime factory...
=========
# MiniMeTokenFactory:
Address: 0xf7d36d4d46cda364edc85e5561450183469484c5
Transaction hash: 0xa54aba97b7253a0ce966f07d20bd70e34b71ba1066c1ab5adff75faabbf33ec9
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-05-24T05:55:24.771Z
=========
```

### Aragon templates

```
=========
# CompanyTemplate:
Address: 0x6015b94e02c6cf3f96c59c8775b252695a00fd9d
Transaction hash: 0x2d6185a7ac9eb67cd01c4b4ab0ed5fe7e7ab09eea858d5274ee543c37049cf03
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-07-11T20:40:36.046Z
=========
0x6015b94e02c6cf3f96c59c8775b252695a00fd9d

=========
# ReputationTemplate:
Address: 0x5651fb1116da6ff7d2ff79af18d8b4439d2ab59f
Transaction hash: 0xbdfb8a5543cae071a32cdecd614b7464aec9ea96c77061bbb28c4ec03695ce39
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-08-13T16:36:56.769Z
=========

=========
# MembershipTemplate:
Address: 0xe7ce233fa80811caa7a290c73ea1d43787868692
Transaction hash: 0x7f2bd4acf74d611315c5df532ec75101054660ed4582444176c3526916fedbfc
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-07-11T23:26:58.034Z
=========

=========
# BareTemplate:
Address: 0xf66eb91773f7c51dc65b31259952e3bd98cb1207
Transaction hash: 0x5381adc5736b55e5adf1721cd8d446ad07abb8881e1eadecf4a2ad4e2a2c8461
Compiler: solc@0.4.24+commit.e67f0147.Emscripten.clang (Optimizer: 10000 runs)
Compiled at: 2020-07-24T14:33:19.589Z
=========

```
