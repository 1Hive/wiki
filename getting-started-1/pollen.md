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

El pago semanal está determinado por la contribución reciente de un contribuyente, así como por su contribución total.

* La **contribución semanal** es la cantidad distribuida por el pollen ganado por los usuarios en la última semana. 
* La **contribución total** es la cantidad distribuida por todo el pollen ganado por los usuarios hasta la fecha de distribución. 
* La **tasa de decaimiento** es la tasa a la que decae el cálculo de la contribución total para cada semana anterior. Por ejemplo, para una tasa de deterioro del 40%, la semana anterior se pondera al 100%, la segunda semana anterior se pondera al 60%, la tercera semana anterior se pondera al 36%, etc.

| Parametro de Distribución | Asignación y Tasa |
| :--- | :--- |
| Contribución Semanal | 25 HNY |
| Contribución Total | 8 HNY |
| Tasa de Decaimiento | 40% |

### Distribución por Plataforma

Un desglose de la distribución relativa de pollen de cada plataforma cada semana.

| Plataforma | Porcentaje de Distribución |
| :--- | :--- |
| GitHub | 40% |
| Discord | 30% |
| Forum | 30% |

### Pesos de Pollen en Discord

En Discord, para generar cred para otros usuarios a través de emojis, los usuarios deben haber recibido algo de cred en el pasado. Generar cred a uno mismo está deshabilitado y el sistema también pondera la cantidad de generación de cred  a otros dependiendo de cuánto cred haya ganado.

| Cred Total | Peso de Acuñado \(mint\) |
| :--- | :--- |
| 120+ Cred  | 1x |
| 90+ Cred | 0.75x |
| 60+ Cred | 0.5x |
| 30+ Cred  | 0.25x |
| 0 to 30 Cred  | 0x |

Todos los emojis dan 1 cred aparte de las siguientes excepciones.

| Emojis | Peso de Acuñado \(mint\) |
| :--- | :--- |
|  🍯 + `:Honeypot:` \(custom emoji\) | 2x |
| 🐝 + `:Honeybee:` \(custom emoji\) | 2x |
| 💩 | 0x |
| 👎 | 0x |

Los canales que dan 0 cred incluyen: ✅**check-in**, ****🐸**memes**, **🤖bot-commands**, **🕹arcade**, **🦩lounge**, **🍱kitchen**, **Fauna** y todos los canales de **Información**.

El canal de  🐝**marketing** channel da 0.25x del peso de cred estandar.

El canal  🍄**nominations** genera 95% de cred a los usuarios que han sido etiquetados en mensajes. Los usuarios que comparten un usuario etiquetado obtienen un 5% de cred por las respuestas. Todos los usuarios etiquetados compartirán cred por igual entre todos los usuarios etiquetados en ese mensaje. 

### Peso de Pollen en el Foro

En el Foro, el cred total que un usuario puede generar depende del nivel de confianza del usuario.

| Nivel de Confianza | Peso de Acuñado \(mint\) |
| :--- | :--- |
| 4 | 1.5x |
| 3 | 1.25x |
| 2 | 1x |
| 1 | 0.1x |
| 0 | 0x |

## Reglas

Debido a lo joven  del software SourceCred, todavía hay algunas formas de explotarlo. Varios cambios de parámetros han minimizado este riesgo, pero 1Hive aún impone las siguientes reglas, que son conocidas y monitoreadas por muchos en la comunidad.

1. **Política de una cuenta por usuario** Un usuario no puede tener ni operar varias cuentas. 
2. **No se permite el intercambio de reacciones** No se permite entablar acuerdos con otros usuarios para reacciones a las publicaciones de los demás. El intercambio de reacciones se define por un patrón de 2 o más usuarios que reaccionan mutuamente a la mayoría o todas las publicaciones de los demás, independientemente de la calidad del contenido.
3. **Abuso de errores / Exploits / Manipulación** Si encuentras un bug o una vulnerabilidad en el sistema, infórmalo de inmediato. Aquellos que utilizan un bug o un exploit en su beneficio corren el riesgo de que su cuenta sea desactivada.

## Links Útiles

Actualizaciones previas y en curso de los [parámetros de pollen](https://forum.1hive.org/t/updates-to-sourcecred/726).

[Reglas generales](https://forum.1hive.org/t/pollen-rules-and-a-reporting-system/1155) para participar en polen.

[Documentación de SourceCred](https://sourcecred.io/docs/) para obtener más información.

