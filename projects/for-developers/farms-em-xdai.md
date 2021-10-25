# Farms em xDai

## **O token xComb**

**O token xComb é o token de incentivo local para Honeyswap em xDai.**

O valor de xComb é derivado da atividade de negociação que ocorre na Honeyswap em xDai por meio de recompensas automatizadas vinculadas às taxas de troca. Metade dos tokens xComb comprados são incinerados, a outra metade é reciclada e retorna às farms para distribuições futuras. O token xComb tem suprimento fixo e torna-se deflacionário por causa da incineração de metade das recompras do token.

### **Suprimento e emissão do xComb**

O fornecimento fixo total dos tokens xComb e de 1,000,000 . Um airdrop inicial de 5% do suprimento total foi distribuído entre provedores de liquidez da Honeyswap, proporcionalmente ao tempo e valor de liquidez contribuída antes do airdrop. 10% dos tokens distribuídos no airdrop são imediatamente líquidos e os 90% restantes serão liberados ao longo de 6 Meses.&#x20;

Os 95% restantes do fornecimento total de xComb serão distribuídos através de farming ao longo de 2 anos, a taxa de emissão decai linearmente de forma que, ao final do período de emissão inicial, a taxa será de 25% da taxa inicial.&#x20;

1% das emissões do xComb pode ser obtida através de indicação de pessoas as farms, incentivando integração e promoção. O restante das emissões é dividido entre pares de troca na Honeyswap proporcionalmente aos seus pontos alocados. Os pontos alocados serão ajustados ao longo do tempo para atrair traders e maximizar o volume da Honeyswap. A tabela a seguir mostra a distribuição atual dos pontos alocados entre os pares.

| Pares      | Pontos |   |
| ---------- | ------ | - |
| xDAI-xComb | 20     |   |
| xDAI-HNY   | 5      |   |
| xDAI-AGVE  | 5      |   |
| HNY-AGVE   | 3      |   |
| HNY-WETH   | 3      |   |
| xDAI-STAKE | 2      |   |
| xDAI-LINK  | 2      |   |
| WETH-WBTC  | 2      |   |
| xDAI-WETH  | 2      |   |
| USDC-xDAI  | 1      |   |

Os pares serão ajustados ao longo do tempo, uma estrutura para avaliar a adicionar pares está sendo desenvolvida. Fique ligado!



## **Governança**

Os contratos AMM da Honeyswap não são atualizáveis. A governança é limitada à definição do endereço receptor das taxas.

O token xComb não possui governança, tem um suprimento limitado e não pode ser atualizado.

O contrato de farming do xComb não pode ser atualizado, mas os tokens mantidos no contrato podem ser retirados através de governança a fim de enviar as recompensas para novos contratos. A governança das fazendas foi dividida em duas funções utilizando um contrato wrapper.

**Gerente: **Pode adicionar, remover e ajustar pontos de alocação dos fundos de liquidez.

**Administrador:** Pode alterar o endereço do gerente e inicializar a migração, retirando xComb e desbloqueando todos os depósitos bloqueados por tempo.

Inicialmente, a [Tulip swarm multisig](https://xdai.gnosis-safe.io/app/#/safes/0xD5a0d695589Fa9dEC023638b8dD24D71f051C63C/balances) servirá como Gerente e a 1Hive [Decisions](https://wiki.1hive.org/projects/honey/decisions) será a Administradora.



## **Contratos das farms**

**xComb** **token:** [0x38Fb649Ad3d6BA1113Be5F57B927053E97fC5bF7​](https://blockscout.com/poa/xdai/address/0x38Fb649Ad3d6BA1113Be5F57B927053E97fC5bF7/read-contract)

**xCombFarm:** [0xB44825cF0d8D4dD552f2434056c41582415AaAa1​](https://blockscout.com/poa/xdai/address/0xB44825cF0d8D4dD552f2434056c41582415AaAa1/read-contract)

**xCombFarm Governance Wrapper: **[0xfBA19af3bE412E08AF9c7Cf60756d238D3cEAd25](https://blockscout.com/poa/xdai/address/0xfBA19af3bE412E08AF9c7Cf60756d238D3cEAd25/read-contract)**​**

**xCombAirdrop: **[0xdD36008685108aFafc11F88bBc66C39A851Df843](https://blockscout.com/poa/xdai/address/0xdD36008685108aFafc11F88bBc66C39A851Df843/read-contract)**​**

**FeeReceiver:** [0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7​](https://blockscout.com/xdai/mainnet/address/0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7/transactions)



### **Subgraphs**

**​**[**Farms Subgraph on xDai**](https://api.thegraph.com/subgraphs/name/1hive/honeyfarm-xdai)**. **[**Source code**](https://github.com/1Hive/honeyfarm-subgraph)**.**















