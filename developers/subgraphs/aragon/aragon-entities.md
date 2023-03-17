# Aragon Entities

* ``[`RegistryFactory`](aragon-entities.md#registryfactory)``
* ``[`Registry`](aragon-entities.md#registry)``
* ``[`Repo`](aragon-entities.md#repo)``
* ``[`Version`](aragon-entities.md#version)``
* ``[`OrgFactory`](aragon-entities.md#orgfactory)``
* ``[`Organization`](aragon-entities.md#organization)``
* ``[`App`](aragon-entities.md#app)``
* ``[`Implementation`](aragon-entities.md#implementation)``
* ``[`Role`](aragon-entities.md#role)``
* ``[`Permission`](aragon-entities.md#permission)``
* ``[`Param`](aragon-entities.md#param)``

### RegistryFactory <a href="#registryfactory" id="registryfactory"></a>

| Field         | Type          | Description                                                          |
| ------------- | ------------- | -------------------------------------------------------------------- |
| id            | ID!           | RegistryFactory address                                              |
| address       | Bytes!        | RegistryFactory address                                              |
| registryCount | Int!          | The number of proxies deployed for the registry factory in this repo |
| registries    | \[Registry!]! | Registries                                                           |

### Registry <a href="#registry" id="registry"></a>

| Field     | Type             | Description                                                  |
| --------- | ---------------- | ------------------------------------------------------------ |
| id        | ID!              | Registry id                                                  |
| address   | Bytes!           | Registry address                                             |
| name      | String!          | Registry name                                                |
| node      | Bytes!           | ENS node                                                     |
| repoCount | Int!             | The number of proxies deployed for the registry in this repo |
| repos     | \[Repo!]!        | Registry repo                                                |
| factory   | RegistryFactory! | Factory registry                                             |

### Repo <a href="#repo" id="repo"></a>

| Field    | Type         | Description                                             |
| -------- | ------------ | ------------------------------------------------------- |
| id       | ID!          | Repo id                                                 |
| address  | Bytes!       | Repo address                                            |
| name     | String!      | Repo name                                               |
| node     | Bytes!       | Repo ENS node                                           |
| versions | \[Version!]! | Repo version                                            |
| registry | Registry!    | Repo registry                                           |
| appCount | Int!         | The number of proxies deployed for the app in this repo |

### Version <a href="#version" id="version"></a>

| Field           | Type    | Description                             |
| --------------- | ------- | --------------------------------------- |
| id              | ID!     | Concat repo address ‘-’ semanticVersion |
| semanticVersion | String! | Semver version number                   |
| codeAddress     | Bytes!  | App implementation address              |
| contentUri      | String! | Content URI, ipfs hash or html url      |
| artifact        | String  | Artifact.json metadata                  |
| manifest        | String  | Manifest.json metadata                  |
| repo            | Repo!   | Version repo                            |
| apps            | \[App!] | App version                             |

### OrgFactory <a href="#orgfactory" id="orgfactory"></a>

| Field         | Type              | Description            |
| ------------- | ----------------- | ---------------------- |
| id            | ID!               | OrgFactory id          |
| address       | Bytes!            | OrgFactory address     |
| orgCount      | Int!              | Number of organzations |
| organizations | \[Organization!]! | Organizations          |

### Organization <a href="#organization" id="organization"></a>

| Field         | Type            | Description                    |
| ------------- | --------------- | ------------------------------ |
| id            | ID!             | Kernel address                 |
| address       | Bytes!          | Organization address           |
| createdAt     | BigInt!         | Block organization was created |
| acl           | Bytes!          | Acl address                    |
| recoveryVault | Bytes!          | Recovery vault address         |
| permissions   | \[Permission!]! | Permissions granted to app     |
| factory       | OrgFactory!     | Organization factory           |

### App <a href="#app" id="app"></a>

| Field          | Type            | Description                       |
| -------------- | --------------- | --------------------------------- |
| id             | ID!             | App proxy address                 |
| address        | Bytes!          | App address                       |
| name           | String!         | App name                          |
| appId          | String!         | ENS namehash of the aragonPM repo |
| implementation | Implementation! | App base implementation entity    |
| isForwarder    | Boolean!        | Whether the app is Forwarder      |
| isUpgradeable  | Boolean!        | Whether the app is upgradeable    |
| version        | Version         | Repo Version entity               |
| repo           | Repo            | App repo                          |
| roles          | \[Role!]!       | Role assigned                     |
| organization   | Organization!   | Organizations in relation to app  |

### Implementation <a href="#implementation" id="implementation"></a>

| Field   | Type   | Description                  |
| ------- | ------ | ---------------------------- |
| id      | ID!    | Concat namespace ‘-’ appId # |
| address | Bytes! | Implementation address       |

### Role <a href="#role" id="role"></a>

| Field    | Type            | Description                      |
| -------- | --------------- | -------------------------------- |
| id       | ID!             | Concat app address ‘-’ role hash |
| hash     | Bytes!          | Role ens namehash                |
| manager  | Bytes!          | Role manager address             |
| app      | App!            | App used for role                |
| grantees | \[Permission!]! | Grantee derived from role        |

### Permission <a href="#permission" id="permission"></a>

| Field          | Type       | Description                                             |
| -------------- | ---------- | ------------------------------------------------------- |
| id             | ID!        | Concat of app address ‘-’ role hash ‘-’ grantee address |
| granteeAddress | Bytes!     | Address assigned the permissions                        |
| allowed        | Boolean!   | Whether the grantee is allowed by the permission        |
| params         | \[Param!]! | List of parameters the permission has                   |
| app            | App!       | App used to request permission                          |
| role           | Role!      | Role in relation to permission                          |

### Param <a href="#param" id="param"></a>

| Field         | Type    | Description                    |
| ------------- | ------- | ------------------------------ |
| id            | ID!     | Concat of param hash ‘-’ index |
| argumentId    | Int!    | Argument id (uint8)            |
| operationType | Int!    | Operation type (uint8)         |
| argumentValue | BigInt! | Argument Value (uint240)       |
