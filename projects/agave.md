---
description: Protocolo de empréstimos
---

# Agave

{% hint style="warning" %}
Esta página reflete a [proposta inicial do Agave](https://forum.1hive.org/t/announcing-agaave-aave-on-xdai/1792). O protocolo ainda está em desenvolvimento e esta página pode estar incompleta ou imprecisa.
{% endhint %}

## Visão geral

Agave é um protocolo de mercado financeiro descentralizado e sem custo, onde usuários podem participar como investidores ou requerendo empréstimos. Agave é um fork de [Aave](https://aave.com) em xDai.

Investidores fornecem liquidez ao mercado para obter uma renda passiva, enquanto mutuários podem pedir empréstimos de uma forma sobre-colateralizada ( perpetuamente) ou de uma forma sub-colateralizada ( liquidez de um bloco, empréstimos instantâneos, por exemplo).

## **Como funciona?**

Usuários depositam tokens no protocolo e recebem um token aToken em retorno. Em seguida, esse token acumula juros. Além disso, ao depositar, usuários podem permitir que seu depósito seja utilizado como garantia e, assim, utilizá-lo para emprestar outros ativos. Isso é funcionalmente o equivalente a oferecer facilidade de alavancagem. Por exemplo, caso um usuário deposite HNY, ele poderá usá-lo como garantia para emprestar DAI e comprar mais HNY.

## **Capacidades**

### **Empréstimos**

Usuários podem emprestar tokens ao protocolo. Juros são determinados dinamicamente pela taxa de utilização do token no protocolo. Assim, à medida que a oferta do token diminui, a taxa de juros aumenta.

### **Requerimento de empréstimos**

Após um usuário requerer um empréstimo utilizando o protocolo, ele terá uma linha de crédito disponível.

### **Empréstimo delegado**

Os credores podem estender sua linha de crédito para outros endereços. Isso efetivamente abre a possibilidade aos usuários que não tem nada depositado no Agave emprestarem do protocolo sem capital.

### **Empréstimos instantâneos**

Os empréstimos instantâneos do Agave são melhores do que a maioria dos oferecidos na mainnet. Usuários podem pegar vários tokens emprestados na mesma transação. Além disso, os empréstimos instantâneos no Agave não necessitam pagamento total na mesma transação: parte do empréstimo pode ser adicionada como dívida se o usuário tiver garantia suficiente no protocolo.



## **Token**

O Agave tem um token utilizado principalmente na governança sobre o protocolo. Veja seguir suas funções:

**• **Adicionar e remover tokens do mercado&#x20;

•Ativar e desativar a capacidade da utilização de tokens específicos como garantia.&#x20;

•Definir taxas de garantia LTV máximo ( Loan to value rate ou, taxa de empréstimo ao valor)&#x20;

•Limite de liquidação&#x20;

•Penalidade na liquidação&#x20;

•Utilização como garantia empréstimo estável

O token também pode ser depositado, o que dá aos que possuem Agave a possibilidade de obter rendimento com o próprio token. O conjunto de tokens depositados é utilizado como seguro no caso de déficit.

## **Como isso beneficia a 1Hive?**

Atualmente, temos a Honeyswap, que permite aos usuários a negociação em xDai com taxas de transação extremamente baixas. Dado o volume relativamente baixo, as taxas totais geradas na Honeyswap são bastante baixas ( 0,3% por transação) e, estas taxas subsidiam os provedores de liquidez, permitindo-lhes gerar HNY. Isso teve resultados mistos.&#x20;

Com o Agave, permitimos que usuários ganhem um rendimento em tokens utilizados na liquidez da Honeyswap sem um subsídio em HNY. Ele também adiciona incentivos extras aos provedores de liquidez, dando-lhes um fluxo adicional de receita acima das taxas geradas na Honeyswap.&#x20;

Um dos recursos mais poderosos em DeFi é a sua capacidade de composição. Atualmente, a Honeyswap não pode ser combinada com outros protocolos de DeFi porque está em uma rede separada. Com o Agave, agora temos outro protocolo em xDai, tornando-o mais "aderente''.

Embora seja um fork de Aave, nós vamos usá-lo como base para um protocolo que se adapte às necessidades da comunidade 1Hive.

A listagem do token Agave será mais simples do que no Aave. Através do Celeste, qualquer pessoa pode adicionar um token ao mercado depositando Agave. Caso um token não atenda ao  [Acordo Aragon](https://aragon.org/agreements) associado, Celeste pode ser utilizado para contestar.

Estas são algumas maneiras pelas quais o Agave fornecerá mais utilidade ao HNY, fazendo assim seu valor crescer.
