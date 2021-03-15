---
description: Gagnez du Honey en contribuant
---

# Pollen

Le Pollen est un classement de contribution utilisé pour reconnaître les contributions sur les  ****communautés 1Hive \([Discord](https://discord.com/invite/P4rRDUKTAU),[ Forum](https://forum.1hive.org/), et[ Github](https://github.com/1Hive)\). Ces contributions sont récompensées avec des distributions hebdomadaires de Honey.

## **Comment participer**

Dès que vous interagissez sur les communautés 1Hive \(Discord, Forum et Github\), vous commencerez à gagner du Pollen, qui sera envoyé dans votre portefeuille enregistré en délicieux Honey !

Afin de recevoir des distributions hebdomadaires de pollen, vous devrez créer des comptes sur les plates-formes prises en charge et les associer à votre adresse xDai. Vous pouvez le faire en publiant ce qui suit sur la chaîne [ 🐛**onboarding**](https://discord.gg/eYwxwv4nzk) du Discord 1hive :

```text
#🏵pollen
github: justabee
discourse: justabee
discord: justabee#1234
xDai: 0x0...000
```

Remplacez`justabee`, `justabee#1234` et `0x0...000` avec vos comptes. `Discourse` fait référence au [Forum](https://forum.1hive.org/).

Si vous avez des questions, souhaitez savoir comment le pollen est calculé ou vérifier les distributions, il vous suffit d’aller sur la chaîne [🏵**pollen**](https://discord.com/invite/y8fPNcNdAa).

## Distribution de Pollen

Le pollen est calculé à l'aide de **SourceCred**, qui sert à créer et analyser un graphique des interactions entre les membres de la communauté. Bien que n'étant pas une représentation parfaite de la valeur des contributions, le pollen peut aider à récompenser les interactions qui sont importantes mais trop granulaires pour justifier la création de propositions ou la revendication d'un essaim.

SourceCred analyse les messages et contributions sur Discord, le forum et GitHub et applique un multiplicateur à un score de base de 1 cred par action. L'un des principaux moyens de gagner du cred est lorsque le texte que vous écrivez ou les actions que vous faites reçoivent une réponse positive des autres membres grâce à l'utilisation d'emojis. Ecrire des messages à lui seul ne fait pas gagner pas de cred. Les pondérations pour la distribution de cred sont décidées par la communauté 1Hive.

Le cred gagné sur 1Hive n’est utile que sur 1Hive. Il n'est pas transférable et la notation est rétroactive, donc si vous vous inscrivez au pollen après en avoir gagné, vous recevrez toujours du cred pour cette période \(vous recevrez une récompense en Honey pour votre cred dès la période après votre inscription\).

Le [Pollen Explorer](https://1hive.github.io/pollen/#/explorer) propose un classement des utilisateurs de Pollen affichant le cred qu'ils ont gagné tout au long de leur engagement avec 1Hive.Les pondérations déterminant le Pollen gagné pour chaque action peuvent être vues dans [l'explorateur de pollen](https://1hive.github.io/pollen/#/explorer) en cliquant sur "SHOW WEIGHT CONFIGURATION".

![](../.gitbook/assets/image%20%288%29.png)

### Distribution totale

La distribution hebdomadaire de Honey est plafonnée à $15’000 ou 33 HNY si 33 HNY valent moins de $15’000. 5% de la distribution hebdomadaire va directement à l'équipe SourceCred.

![Figure 1. Distribution hebdomadaire de HNY en fonction de la valeur en USD](../.gitbook/assets/image%20%2814%29.png)

### Taux de distribution

Le paiement hebdomadaire est déterminé par la contribution récente d'un contributeur ainsi que sa contribution totale.

* **La contribution hebdomadaire** est le montant distribué pour le pollen gagné par les utilisateurs au cours de la semaine dernière.
* **La contribution totale** est le montant distribué pour tout le pollen gagné par les utilisateurs de leur inscription jusqu'à la date de distribution.
* **Le taux de décroissance** est le taux auquel le calcul de la contribution totale diminue pour chaque semaine précédente. Par exemple, pour un taux de décroissance de 40%, la semaine précédente est pondérée à 100%, la deuxième semaine précédente est pondérée à 60%, la troisième semaine précédente est pondérée à 36%, etc.

| Paramètre de distribution | Allocation & taux |
| :--- | :--- |
| Contribution hebdomadaire | 25 HNY |
| Contribution totale | 8 HNY |
| Taux de décroissance | 40% |

### **Distribution par plate-forme**

Une vue de la distribution relative de Pollen sur chaque plate-forme chaque semaine.

| Plate-forme | Pourcentage de distribution |
| :--- | :--- |
| GitHub | 30% |
| Discord | 40% |
| Forum | 30% |

### Pondération sur Discord

Sur Discord, pour donner du cred à d'autres utilisateurs via des réponses emoji, les utilisateurs doivent avoir déjà reçu du cred auparavant. On ne peut pas s’auto récompenser en cred. La quantité de cred d’un membre influence la quantité de cred qu’il peut émettre.

| Cred total | Pondération |
| :--- | :--- |
| 120+ Cred | 1x |
| 90+ Cred | 0.75x |
| 60+ Cred | 0.5x |
| 30+ Cred | 0.25x |
| 0 à 30 Cred | 0x |

Tous les emojis donnent 1 cred, sauf les exceptions ci-dessous.

| Emoji | Pondération |
| :--- | :--- |
| 🍯 + `:Honeypot:` \(emoji ****custom\) | 2x |
| 🐝 + `:Honeybee:` \(emoji custom\) | 2x |
| 💩 | 0x |
| 👎 | 0x |

Les chaînes qui donnent 0 cred incluent : **✅check-in, 🐸memes, 🤖bot-commands, 🕹arcade, 🦩lounge, 🍱kitchen, 🐱Fauna** et les chaînes d’**information.**

La chaîne **🐝social-curation** donne 0,25x le cred standard.

La chaîne **🍄nominations** donne 95% du cred aux membres tagués dans les messages. Les utilisateurs nommant un membre obtiennent 5% du cred. Tous les membres tagués dans un message partageront le cred de manière égale.

### Pondération sur le forum

Sur le forum, le cred total qu'un utilisateur peut obtenir dépend du niveau de confiance de l'utilisateur. \(trust level\)

| Trust level | **Pondération** |
| :--- | :--- |
| 4 | 1.5x |
| 3 | 1.25x |
| 2 | 1x |
| 1 | 0.1x |
| 0 | 0x |

## **Règles**

Comme le logiciel SourceCred est encore récent, il existe encore des moyens de tricher. ****Divers changements de paramètres ont minimisé ce risque, mais 1Hive impose toujours les règles suivantes, qui sont connues et surveillées par de nombreux membres de la communauté.

1. **Un compte par utilisateur** Un utilisateur n'est pas autorisé à posséder et à gérer plusieurs comptes.
2. **Interdiction d’échanger des réactions ou des likes** Les accords avec d'autres utilisateurs pour aimer / réagir aux messages de l'autre ne sont pas autorisés. Le trading de réactions / likes est défini par un modèle d'au moins 2 utilisateurs réagissant mutuellement à la plupart ou à la totalité des messages de chacun, quelle que soit la qualité du contenu.
3. **Utilisation de bogues / Exploits / Manipulation** Si vous trouvez un bogue ou un exploit dans le système, veuillez le signaler immédiatement. Ceux qui utilisent un bogue ou un exploit à leur avantage risquent la désactivation de leur compte.

## **Liens utiles**

[Mises à jour](https://forum.1hive.org/t/updates-to-sourcecred/726) précédentes et en cours des paramètres du pollen.

[Règles générales](https://forum.1hive.org/t/pollen-rules-and-a-reporting-system/1155) pour s'engager dans le pollen.

[Documentation SourceCred](https://sourcecred.io/docs/) pour plus d'informations.

