---
description: Gana Honey por tus contribuciones
---

# Pollen

El pollen \(polen\) es un rango de contribuyente que se utiliza para reconocer las contribuciones a las comunidades de [Discord](https://discord.com/invite/P4rRDUKTAU), [Forum](https://forum.1hive.org/), y [Github](https://github.com/1Hive) de 1Hive, y recompensar estas contribuciones con distribuciones semanales de Honey. 

## Como participo

Tan pronto como comiences a interactuar en las comunidades de Discord, Forum y Github de 1Hive, comenzarás a ganar pollen, que se agrega a tu billetera registrada como dulce dulce Honey. 

Para recibir distribuciones de pollen semanales, deberás crear cuentas en plataformas compatibles y vincularlas a tu dirección xDai. Puedes hacer esto publicando lo siguiente en el canal [🐛**onboarding**](https://discord.gg/eYwxwv4nzk) de 1hive Discord:

```text
#🏵pollen
github: justabee
discourse: justabee
discord: justabee#1234
xDai: 0x0...000
```

Reemplazando`justabee`, `justabee#1234` y `0x0...000` con tus cuentas. Nota `Discourse` se refiere [al Foro](https://forum.1hive.org/).

Si tiene preguntas, estás interesado en cómo se calcula el pollen o quieres auditar las distribuciones, simplemente acceda al canal [🏵**pollen**](https://discord.com/invite/y8fPNcNdAa)**.**

## Distribución de Pollen

El pollen se calcula utilizando **SourceCred** para crear y analizar un gráfico de interacciones entre los miembros de la comunidad. Si bien no es una representación perfecta del valor de las contribuciones, Pollen puede ayudar a recompensar las interacciones que son importantes pero demasiado granulares para justificar la creación de propuestas o reclamos de un Swarm.

SourceCred monitorea todos los mensajes y contribuciones a Discord, el Foro y GitHub y aplica un multiplicador a una puntuación base de 1 cred por acción. Una de las principales formas de ganar cred es cuando el texto que escribes o las acciones que creas son respondidas de manera positiva por otros miembros mediante el uso de emojis. Escribir mensajes por sí solo no gana cred. Los pesos para la distribución de Cred los decide la comunidad de 1Hive. 

El cred obtenido en 1Hive solo es útil dentro de 1Hive. No es transferible y la puntuación es retroactiva, por lo que si te registras en pollen después de haber ganado algo, aún recibirás cred por ese período \(aunque solo recibirás una recompensa de Honey por tu crédito por el período después de registrarte\).

[El Explorador de Pollen](https://1hive.github.io/pollen/#/explorer) tiene una tabla de clasificación de usuarios de Pollen que muestran el cred que se han ganado a lo largo de su compromiso con 1Hive.

Los pesos que determinan el Pollen ganado por cada acción se pueden ver en el [explorador de pollen](https://1hive.github.io/pollen/#/explorer) haciendo clic en "SHOW WEIGHT CONFIGURATION".

![](../.gitbook/assets/image%20%288%29.png)

### Distribución Total

La distribución semanal de Honey tiene un límite de $15,000 o 33 Honey si 33 Honey vale menos de $15,000. El 5% de la distribución semanal va directamente al equipo de SourceCred. 

![Figura 1. Distribuci&#xF3;n semanal en Honey basada en el valor del USD](../.gitbook/assets/image%20%2814%29.png)

### Tasa de Distribución

Weekly payout is determined by a contributor's recent contribution's as well as their total contribution. 

* **Weekly contribution** is the amount distributed for Pollen earned by users in the last week.
* **Total contribution** is the amount distributed for all Pollen earned by users up to the distribution date.
* **Decay Rate** is the rate at which the total contribution calculation decays for each previous week. Eg for a decay rate of 40%, the previous week is weighted at 100%, the second previous week is weighted at 60%, the third previous week is weighted at 36%, etc.

| Distribution Parameter | Allocation & Rate |
| :--- | :--- |
| Weekly Contribution | 25 HNY |
| Total Contribution | 8 HNY |
| Decay Rate | 40% |

### Platform Distribution

A breakdown of each platforms relative distribution of Pollen each week.

| Platform | Percent of Distribution |
| :--- | :--- |
| GitHub | 40% |
| Discord | 30% |
| Forum | 30% |

### Discord Pollen Weights

On Discord, in order to mint cred for other users through emoji responses, users must have received some cred in the past. Minting to self is disabled and the system also weights the minting amount to others depending on how much cred the minter has earned.

| Total Cred | Mint Weight |
| :--- | :--- |
| 120+ Cred  | 1x |
| 90+ Cred | 0.75x |
| 60+ Cred | 0.5x |
| 30+ Cred  | 0.25x |
| 0 to 30 Cred  | 0x |

All emojis give 1 cred, apart from the below exceptions.

| Emoji | Mint Weight |
| :--- | :--- |
|  🍯 + `:Honeypot:` \(custom emoji\) | 2x |
| 🐝 + `:Honeybee:` \(custom emoji\) | 2x |
| 💩 | 0x |
| 👎 | 0x |

Channels that give 0 cred include: ✅**check-in**, ****🐸**memes**, **🤖bot-commands**, **🕹arcade**, **🦩lounge**, **🍱kitchen**, **Fauna** channels and all of the **Information** channels.

The 🐝**marketing** channel gives 0.25x the standard cred weight.

The 🍄**nominations** channel mints 95% of cred for users who have been tagged in messages. Users sharing a tagged user get 5% cred for responses. All users tagged will share cred equally amongst all tagged users in that message.

### Forum Pollen Weights

On the Forum the total cred a user can mint is dependent on the trust level of the user.

| Trust level | Mint Weight |
| :--- | :--- |
| 4 | 1.5x |
| 3 | 1.25x |
| 2 | 1x |
| 1 | 0.1x |
| 0 | 0x |

## Rules

Due to the infancy of the SourceCred software there are still some ways to exploit it. Various parameter changes have minimized this risk but 1Hive still imposes the following rules, which are known and monitored by many in the community.

1. **One account per user policy** A user is not allowed to own and operate multiple accounts.
2. **No reactions/likes trading allowed** Entering agreements with other users to like/react to each other’s posts is not allowed. Reactions/Likes trading is defined by a pattern of 2 or more users mutually reacting to most or all of each other’s posts, regardless of the quality of the content.
3. **Bug use / Exploits / Manipulation** If you find a bug or exploit in the system, please report it immediately. Those using a bug or exploit to their advantage may risk account deactivation.

## Useful Links

Previous and ongoing [updates to Pollen parameters](https://forum.1hive.org/t/updates-to-sourcecred/726).

[General rules](https://forum.1hive.org/t/pollen-rules-and-a-reporting-system/1155) for engaging in Pollen.

[SourceCred documentation](https://sourcecred.io/docs/) for further information.

