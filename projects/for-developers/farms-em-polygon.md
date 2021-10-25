# Farms em Polygon

## **O token pComb**

**O token pComb é o token de incentivo local para Honeyswap em Polygon.**

O valor de pComb é derivado da atividade de negociação que ocorre na Honeyswap em Polygon por meio de recompensas automatizadas vinculadas às taxas de troca. Metade dos tokens pComb comprados são incinerados, a outra metade é reciclada e retorna às farms para distribuições futuras. O token pComb tem suprimento fixo e torna-se deflacionário por causa da incineração de metade das recompras do token.



### **pCOMB Suprimento e emissão**

O fornecimento fixo total dos tokens pComb é de 1,000,000 . Um airdrop inicial de 5% do fornecimento fixo total foi distribuído para a comunidade de usuários de DeFi em Polygon, incluindo provedores de liquidez na Honeyswap. 10% dos tokens distribuídos são imediatamente líquidos e os outros 90% restantes são liberados continuamente ao longo de 6 meses .

Os outros 5% do suprimento fixo total foram reservados pelo Tulip Swarm para fins promocionais futuros.

Os 90% restantes do fornecimento de pComb estão programados para serem distribuídos através de farming ao longo de 2 anos, a taxa de emissão decai linearmente de forma que, ao final do período de emissão inicial, a taxa será de 25%. 1% das emissões do pComb pode ser obtida através de indicação de pessoas as farms, incentivando integração e promoção. O restante das emissões é dividido entre pares de troca na Honeyswap proporcionalmente aos seus pontos alocados.

A alocação dos pontos é gerenciada por colaboradores do Tulip Swarm e uma carteira multi-sig. Este privilégio pode ser revogado ou atribuído por meio de voto de decisão utilizando pComb, após a implementação de Gardens, a plataforma de governança onchain da 1Hive para Polygon.

O objetivo do Tulip Swarm em administrar os pontos alocados e promover o crescimento da liquidez e do volume na Honeyswap. Portanto, podemos ajustar os pontos alocados.



## **Nossa política atual**

**Capacidade de alocação de pontos - **optamos por limitar o número total de pontos alocados atribuídos a 1000. Pode haver menos de 1000 pontos atribuídos, mas não mais.

### **Alocação atual**

No momento do lançamento, as fazendas estavam utilizando apenas 575 pontos de um total de 1000 de alocação disponível. À medida que os restantes 425 pontos de alocação são adicionados, as recompensas são diluídas.

**Fundo principal - **Alocamos até **300** pontos para dar suporte ao par pComb-wETH, a fim de garantir que haja um incentivo significativo para fornecer liquidez ao token de recompensa.

**Fundo discricionário - **Nós temos **300** pontos reservados para uso discricionário. Esses pontos foram usados para estabelecer os pares incentivados iniciais.** Após** **4** **meses** de recompensas para farming, esses pontos serão reavaliados e realocados.



### **Alocações projetadas**

Planejamos conduzir programas de incentivos adicionais nos próximos meses usando o sistema de pontos de alocação e, para isso, reservamos pontos de alocação.

**Fundo para traders - **Alocamos **300** pontos para um programa de incentivo de negociações. O objetivo deste programa é recompensar traders que utilizam Honeyswap. Traders receberão pComb periodicamente, proporcional ao volume de negociação na plataforma. Detalhes sobre o programa de recompensas de negociação serão anunciados assim que estiverem disponíveis.

**Fundo de desempenho - **Alocamos 75 pontos para apoiar um programa de recompensa baseado em métrica, onde um conjunto de fundos elegíveis competem por pontos de alocação em uma temporada piloto inicial de 4 meses.

**Fundo de descoberta - **Alocamos 50 pontos para promover tokens novos ou ilíquidos para estabelecer a Honeyswap como o principal local de negociação desses tokens.

### **Tabela atual de pontos alocados para pComb**

| Pares       | Pontos | Categoria      |
| ----------- | ------ | -------------- |
| wETH-pCOMB  | 300    | Keystone       |
| wETH-HNY    | 50     | Discricionário |
| wETH-wMATIC | 50     | Discricionário |
| wETH-wBTC   | 50     | Discricionário |
| wETH-USDC   | 50     | Discricionário |
| wETH-USDT   | 25     | Discricionário |
| wETH-DAI    | 25     | Discricionário |
| wETH-AAVE   | 25     | Discricionário |
| SURF-WAVE   | 13     | Descoberta     |



## **Governança**

O token pComb não possui governança, tem um fornecimento fixo e não pode ser atualizado.

O contrato de farming do pComb não é atualizável, mas seus tokens mantidos pelo contratos podem ser retirados via governança a fim de fazer a transição das recompensas de farming para um novo contrato. A governança das fazendas foi dividida em duas funções distintas usando um contrato de wrap.

**Gerente: **Pode adicionar, remover e ajustar pontos alocados a fundos.

**Administrador: **Pode alterar o endereço do gerente e inicializar uma migração retirando pComb e desbloqueando todos os depósitos bloqueados por tempo.

Inicialmente, o [Tulip swarm multisig ](https://polygon.gnosis-safe.io/app/#/safes/0xD5a0d695589Fa9dEC023638b8dD24D71f051C63C/balances) servirá como gerente e as [Decisões](https://wiki.1hive.org/projects/honey/decisions) da 1Hive controlarão a função de administrador.



## Contratos das farms

**pComb Token: **[0x37d1ebc3af809b8fadb45dce7077efc629b2b5bb](https://polygonscan.com/token/0x37d1ebc3af809b8fadb45dce7077efc629b2b5bb)****

**pComb Farm: **[0x62d7E2484FCFc6752B9473260efE1B86caBAc34e](https://polygonscan.com/address/0x62d7E2484FCFc6752B9473260efE1B86caBAc34e#code)****

**pCombAirdrop: **[0x3Fe30742aD8491402c8aee251ff57e3E9b18Ff87](https://polygonscan.com/address/0x3fe30742ad8491402c8aee251ff57e3e9b18ff87#code)****

****

### **Subgraphs**

**​**[Farms Subgraph on xDai](https://api.thegraph.com/subgraphs/name/1hive/honeyfarm-xdai). [Source code here](https://github.com/1Hive/honeyfarm-subgraph).​​​
