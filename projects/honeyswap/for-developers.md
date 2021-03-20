# Para Programadores

## **HoneySwap**

Honeyswap é uma implantação modificada de Uniswap em xDai  


## **Contratos**

**UniswapV2Factory**:[`0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7`](https://blockscout.com/poa/xdai/address/0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7)\*\*\*\*

**UniswapV2Router02**:[`0x1C232F01118CB8B424793ae03F870aa7D0ac7f77`](https://blockscout.com/poa/xdai/address/0x1C232F01118CB8B424793ae03F870aa7D0ac7f77)

### Front-end

O front-end é implementado em [honeyswap.org](https://honeyswap.org/) e o código fonte pode ser encontrado [aqui](https://github.com/1Hive/uniswap-interface). As maiores modificações são rebranding e uma lista de tokens modificada.  


### Info.honeyswap.org

Um fork da uniswap.info para Honeyswap. Pode ser visto em [info.honeyswap.org](https://info.honeyswap.org/).  


## **Subgraph**

Um fork formado por divisões de dois subgrafos:

[Uniswap v2 subgraph](https://thegraph.com/explorer/subgraph/1hive/uniswap-v2): Um fork do subgraph oficial uniswap v2 com ajustes para usar xDai como moeda base e uma lista modificada de tokens aprovados. o código fonte pode ser encontrado [aqui](https://github.com/1Hive/uniswap-v2-subgraph).

​

[Ethereum Blocks](https://thegraph.com/explorer/subgraph/1hive/xdai-blocks): Um fork do subgraph Blocklytics Ethereum Blocks sem modificações, implementado em xDai. O código fonte pode ser encontrado [aqui](https://github.com/1Hive/ethereum-blocks).  


### Front-end

O front-end  é um fork do código fonte da uniswap.info com modificações para utlizaçāo do Blockscout ao invés do Etherscan, junto com ajustes menores para a utlizaçāo de tokens e seus respectivos endereços de contrato.

O código fonte pode ser encontrado [aqui](https://github.com/1Hive/uniswap-info/).  


### Honeymaker

Honeymaker é uma implementação de SushiMaker e um bot que o acompanha e converte compartilhamentos de LP no Honeyswap em Honey para os recursos comunitários.

Sushimaker está implementado em[ 0x076b64f9F966e3bBD0FCdC79D490Ab71cF961bb0](https://blockscout.com/poa/xdai/address/0x076b64f9F966e3bBD0FCdC79D490Ab71cF961bb0).

O bot ativa periodicamente a função convert no contrato do SushiMaker para determinados pares no Honeyswap para converter LP em Honey.

O código fonte pode ser encontrado aqui.

## **Links Úteis**

[Subgraf da Common pool](https://thegraph.com/explorer/subgraph/onbjerg/honey) \( recursos comunitários\).

