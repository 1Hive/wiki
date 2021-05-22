# Developers

The 1Hive protocol is based on software built by Aragon. The Aragon client interface to the 1Hive DAO is [found here](https://aragon.1hive.org/#/0x8ccbeab14b5ac4a431fffc39f4bec4089020a155). The 1Hive protocol is made up of various Aragon apps tied into the Aragon infrastructure, external contracts and Celeste.

## 1Hive Aragon DAO addresses

```text
DAO/Kernal: 0x8ccbeab14b5ac4a431fffc39f4bec4089020a155
ACL: 0xbc4fb635636b81e60a4e356c4dceb53cac507d03
ConvictionVoting: 0x0b21081c6f8b1990f53fc76279cc41ba22d7afe2
DisputableVoting: 0xfbd0b2726070a9d6aff6d7216c9e9340eae68b2a
Agreement: 0x59a15718992a42082ab2306bc6cbd662958a178c
HookedTokenManager: 0xed062e26c8f41a9088d060156edc7fc6c17d5825
BrightIdRegister: 0x7714eb44754cb9db6d65b61f3352df12600dc593
Agent/Vault: 0x4ba7362f9189572cbb1216819a45aba0d0b2d1cb
StakingFactory: 0xe71331AEf803BaeC606423B105e4d1C85f012C00
Staking (Honey): 0x0e25b918c9fb2fea5d42011d1f4b9f8c61b453e7
```

## External contract addresses

```text
IncentivisedSlidingWindowOracle: 0x6f38D112b13eda1E3abAFC61E296Be2E27F15071
FeesUpdater: 0xeb24f7001437188baF2D5Ef0b0FcFadAD4564517
```

### IncentivisedSlidingWindowOracle

Anyone can update the Honey price used, fetched from Honeyswap, which is used for calculating the value of Honey payouts in stable token funding proposals and calculating Celeste fees. 

To update the price for a particular pair requires calling the `update` function on the [IncentivisedSlidingWindowOracle in Blockscout](https://blockscout.com/poa/xdai/address/0x6f38D112b13eda1E3abAFC61E296Be2E27F15071/write-contract) with the tokens that you want to update the price for. 1Hive runs a service that should call this automatically but it is available for anyone to call. For our purposes we want to call it with the tokens:  
  
Honey `0x71850b7e9ee3f13ab46d67167341e4bdc905eef9`    
Wrapped xDai`0xe91D153E0b41518A2Ce8Dd3D7944Fa863463a97d`

The price oracle requires `update` to be called once every 3 hours for a specific pair. If it is not updated once every 3 hours within the previous 24 hours, calls checking prices will revert.

### FeesUpdater

Anyone can update the Celeste fees, paid for in Honey, but which are defined using a stable amount by calling `updateCourtFees` function on the [FeesUpdater in Blockscout](https://blockscout.com/poa/xdai/address/0xeb24f7001437188baF2D5Ef0b0FcFadAD4564517/write-contract).

## Celeste and modules addresses

```text
Celeste: 0x44E4fCFed14E1285c9e0F6eae77D5fDd0F196f85
Dispute: 0xeC7904e20b69F60966D6c6b9DC534355614dd922
Registry: 0x8C9968a2b16bc1cD0eaD74F5eeF25E899e795501
Voting: 0x1a0d15f1f6d90C2b71EbA3859a1F30c91E5af9b
Treasury: 0xeac1dc5ccF09E2b816F9544878CD513728Fa6af7
Subscriptions: 0x41aB49872ED459C840d0CAecd47FcDC201C48307
```

