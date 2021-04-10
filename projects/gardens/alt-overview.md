# Technical Overview

Gardens is a platform for creating and engaging with tokenized communities. Users can stake tokens to signal attention, prioritize proposals, and collectively allocate shared resources.

### Problem

Tokenized Communities are powerful forces, but reaching majority consensus as a community is difficult and divisive. Voting is expensive \(on Mainnet\) and often only attractive to whales that have high confidence that their vote will be decisive. This has a negative effect on participation, and weakens the feeling of voice and influence that helps nurture a sense of broad community ownership.

### Solution

Gardens enables tokenized communities to more easily leverage conviction voting, a novel consensus process, that proportionally represents the interest of active community members, and for users to more easily participate across a wide range of communities they care about. 

* Traditional online communities that have yet to tokenize, such as open source projects,  can use the platform to tokenize, reward contributions with tokens, and allow patrons to buy tokens and use them to signal priorities by staking on proposals.
* Existing token projects, can use the platform to improve engagement with their communities by directing a portion of onchain cash flows into a community directed pool, or simply allowing token holders to act as patrons, curating and prioritizing important features and milestones. 

### Planned Functionality

* Users will be able to bring an existing ERC20 token or create a new one for their community. 
  * If using an existing ERC20 token, the common pool could be funded via a configurable fee associated with staking or unstaking tokens, or through donations \(eg directing a portion of on-chain cashflow to the common pool\). 
  * If creating a new token, the common pool is funded via a dynamic supply policy just like Honey.
* Users will be able to draft and adopt written community guidelines used for moderating proposals.
  * When creating a proposal users will stake tokens, and other users can challenge them if the proposals violate the communities guidelines. In the event of such a dispute [Celeste](../celeste.md) could be invoked to provide a resolution. 
* Users will be able to browse, discover, and join \(by purchasing tokens on Honeyswap\) communities on an interface provided on [1hive.org](www.1hive.org).
  * The ranking of communities in this list will be determined by the amount of Honey held in the corresponding liquidity pools on Honeyswap.
* Individual communities pages will be accessible at 1hive.org/\#/&lt;community-name&gt;
* Proposal metadata, user profiles, and comments will all be stored on IPFS allowing alternative interfaces to be created and offered in a decentralized and permissionless fashion. 
  * To remain visible on the interface that is made available on 1hive.org, users and communities would need to adhere to the 1Hive Community Covenant. 

