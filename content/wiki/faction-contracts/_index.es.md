---
title: "Contratos de Facción"
date: 2022-12-05T10:30:49+02:00
---

## Información general

De vez en cuando, los agentes de tu [facción](/wiki/packages-factions/#factions) te enviarán una lista de ofertas de contratos. Estos contratos abarcan una variedad de tareas que tendrás que cumplir, pero otorgarán recompensas en forma de moneda, materiales o reputación de la facción. Aceptar estos contratos es opcional.

## Recibir y aceptar contratos de facción

Una vez que hayas encontrado tu primera base, los agentes de tu facción se pondrán en contacto contigo con ofertas de contratos. Estas ofertas suelen venir en lotes de tres. Recibirás una notificación y los contratos aparecerán en tu comando `CONTS` en el estado `open`.

![CONTS](./conts.png)

Puedes revisar cada contrato haciendo clic en el comando de vista. Aunque hay ciertos tipos de contratos, cada contrato es un poco diferente, así que asegúrate de revisarlo adecuadamente antes de aceptar uno.

Aquí hay un ejemplo de contrato:

![CONT example](./cont_example.png)

El preámbulo se divide en dos secciones. La parte 'Ofertas de Contratos de Facción' describe cómo este contrato es parte de una oferta de contrato y tiene enlaces a las otras ofertas de contrato. 

La segunda parte 'Descripción de la Misión' tiene una descripción textual de la misión y es básicamente un resumen de las condiciones del contrato listadas a continuación.

En este punto tienes tres opciones:
* **Aceptar** el contrato. El contrato pasará de `open` a `closed` y se comportará como cualquier otro contrato.
* **Rechazar** el contrato. Esto marcará el contrato como `rejected`.
* **Esperar**. Después de 48 horas, los contratos `open` se cancelan automáticamente.

{{% notice style="primary" title="Aceptar una oferta de contrato" icon="exclamation" %}}
Ten en cuenta que aceptar una de las ofertas de contrato cancelará automáticamente las otras ofertas de contrato. 
{{% /notice %}}

## Recompensas y reputación

Aceptar y cumplir contratos de facción es opcional. No hay desventajas en ignorarlos o rechazarlos, aparte de no recibir las recompensas y la reputación de la facción.

Existen tipos de contratos de facción que son muy comunes, como el ejemplo mostrado arriba, pero de vez en cuando recibirás un tipo más raro. Cuanto más raro sea el tipo de contrato, mayores serán sus recompensas.

Los contratos de facción ofrecen una combinación de recompensas en forma de moneda, bienes y puntos de reputación de la facción.

La cantidad de recompensa monetaria depende del tipo de contrato y de la presencia de una recompensa en bienes. Por lo general, la recompensa monetaria es menor si también hay una recompensa en bienes presente.

Las recompensas en bienes siempre deberán recogerse en la ubicación de tu sede.

Cumplir con éxito los contratos de facción otorgará puntos de reputación de la facción. Todos comienzan con una reputación de facción de 100. Cuanto mayor sea la reputación de la facción, mayores serán las recompensas de los futuros contratos de facción. La reputación actual de la facción se puede ver en el comando `CO`, utilizando el código de tu empresa:

![Reputación de la facción en el comando CO](./reputation.png)

## Desactivar contratos de facción

Si no deseas recibir ofertas de contratos de facción, puedes desactivar las ofertas en el comando `FA` correspondiente. Puedes acceder a él fácilmente haciendo clic en el nombre de un agente de facción.

![Desactivar ofertas de contratos de facción en el comando FA](./disable.png)

{{% about-this-page %}}
