---
description: Programa de recompensas por errores de contrato inteligente
---

# Bug Bounty

Este programa cubre todos los contratos inteligentes relacionados con 1hive que se encuentran implementados en la red xDai que se están utilizando activamente desde la [organización de 1Hive Github](https://github.com/1Hive/). Los contratos que usa 1Hive que no son construidos por miembros de la comunidad de 1hive también pueden ser considerados, dependiendo de la medida en que se hayan utilizado dentro del ecosistema de la comunidad y las consecuencias que podrían producir. Esta evaluación quedará a discreción de los miembros del Bounty Swarm usando la [escala de calificación de riesgo CVSS](https://www.first.org/cvss/calculator/3.0) y los fondos disponibles se mantienen en un DAO de Aragon. Los miembros y un enlace al DAO que tiene los fondos pueden ser vistos en los detalles de [Bug Bounty Swarm](../swarms/bug-bounty.md).

## Requisitos

* La revelación de los bugs debe hacerse directamente a uno de los miembros del Bounty Swarm. Un DM a través de la discord está bien. 
* Cualquier evidencia de divulgación a otras partes hará que se pierda la recompensa. 
* Aprovechar la vulnerabilidad antes de revelarla hará que se pierda la recompensa. 
* La divulgación debe incluir detalles sobre cómo reproducir el error de la manera más clara posible. Un informe más detallado podría aumentar la recompensa. 
* Informar un error que ya se ha informado no obtendrá una recompensa.
* Los errores de front-end no obtendrán recompensas.

## Recompensas

La gravedad de un problema se determinará mediante una puntuación creada utilizando la escala de calificación de riesgo CVSS [https://www.first.org/cvss/calculator/3.0](https://www.first.org/cvss/calculator/3.0). Es probable que también implique una comprensión subjetiva del impacto potencial que podría tener en el ecosistema de 1Hive.

| Calificación de Riesgo | Pago |
| :---: | :---: |
| Critico \(9.0-10.0\): | Hasta $40,000 en HNY |
| Alto \(7.0-8.9\): | Hasta $10,000 en HNY |
| Medio \(4.0-6.9\): | Hasta $2,000 en HNY |
| Bajo \(0.1-3.9\): | Hasta $1,000 en HNY |

Como referencia, habríamos puntuado el exploit que se detalla aquí [Historia de una abeja: por qué se retrasó el Farming](https://forum.1hive.org/t/story-of-a-bee-why-farming-was-delayed/875) con 9.3 ganando hasta $ 40,000 en HNY, la cantidad exacta probablemente debería discutirse, pero habríamos propuesto que estuviera más cerca límite. La puntuación que hemos elegido se puede ver aquí: [https://www.first.org/cvss/calculator/3.0\#CVSS:3.0/AV:N/AC:L/PR:N/UI:R/S:C/C:N/I:H/A:L 3](https://www.first.org/cvss/calculator/3.0#CVSS:3.0/AV:N/AC:L/PR:N/UI:R/S:C/C:N/I:H/A:L)

Debe saberse que 1hive está interesado en mantener una infraestructura segura y está dispuesto a hacer pagos justos por encontrar errores/bugs que podrían afectar los fondos y los usuarios. Estos requisitos y tarifas han sido discutidos y acordados por la comunidad aquí [Propuesta del programa de recompensa de errores de contrato en 1Hive](https://forum.1hive.org/t/1hive-contract-bug-bounty-program-proposal/978) y aquí [Propuesta final del programa de recompensas por errores del contrato en 1Hive](https://forum.1hive.org/t/final-1hive-contract-bug-bounty-program-proposal/1339) para que, como cazador de bugs, puedas estar seguro de que cuando se trata de reclamar una recompensa, la recibirás, siempre que actúes como se describe anteriormente.

