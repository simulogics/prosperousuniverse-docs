---
title: "Infraestructura: Puertas de Enlace"
date: 2025-11-06T17:01:49+02:00
---

## Información General

Las puertas de enlace son un tipo de [infraestructura](../infrastructure) que forman conexiones más rápidas que la luz, lo que permite a las naves viajar entre sistemas que no han sido conectados por conexiones regulares antes. Las puertas de enlace son construidas y operadas por los gobiernos planetarios.

El comando `GTW` proporciona una lista de todas las puertas de enlace. El comando permite filtrar las puertas de enlace por sistema o planeta utilizando un parámetro adicional, por ejemplo: `GTW LS-300` o `GTW LS-300c`.

![Gateway Command GTW](./gateway-command-list.png)

Cuando se proporciona un ID de puerta de enlace, el comando `GTW` mostrará los detalles de la puerta de enlace seleccionada:

![Gateway Command GTW - specific gateway](./gateway-command.png)

## Diseño y construcción de puertas de enlace

El comando `GTWI` (información de la puerta de enlace) permite planificar nuevas puertas de enlace, así como obtener información sobre posibles mejoras para las puertas de enlace existentes.

![Gateway Information](./gateway-gtwi.png)

Las propiedades clave de las puertas de enlace incluyen:

* **Capacidad**: Determina cuántas naves pueden viajar a través de una puerta de enlace en una ventana de 24 horas y cuánto Combustible Vórtice se puede almacenar en una puerta de enlace.
* **Volumen**: Determina el volumen máximo que puede tener una nave (en m³) para poder realizar el salto a través de la puerta de enlace.
* **Distancia**: Determina la distancia máxima que puede tener una puerta de enlace de destino para formar un enlace.

Las tres propiedades se pueden mejorar con una mejora de infraestructura; sin embargo, hay límites: una puerta de enlace puede tener un máximo de cinco mejoras. La capacidad se puede mejorar hasta cinco veces, el volumen y la distancia hasta tres veces.

`GTWI` mostrará los costos de construcción o mejora correspondientes, así como los costos de mantenimiento semanales.

La última sección ofrece una visión general de todos los sistemas que están al alcance de la puerta de enlace con la configuración especificada.

Las puertas de enlace se construyen como cualquier otra infraestructura: el gobierno crea una moción de construcción de infraestructura y nombra a un constructor. Para más detalles, consulte [construcción de infraestructura](./infrastructure/#infrastructure-construction)

## Enlace de puertas de enlace

Los enlaces de puertas de enlace se establecen mediante mociones. El gobierno selecciona la puerta de enlace de origen y una puerta de enlace en el planeta de destino. El componente de la moción mostrará la distancia real del enlace y si la puerta de enlace de origen y destino admite esta distancia. Ambas puertas de enlace deben estar al alcance una de la otra para formar un enlace.

![Moción de Enlace de Puertas de Enlace](./gateway-linking.png)

Una puerta de enlace que aún no se ha vinculado tendrá el estado de enlace `UNLINKED`. Una vez que la moción de enlace haya sido aprobada, el estado de enlace cambia a `INCOMPLETE`. El estado de enlace cambiará a `ESTABLISHED` si la puerta de enlace de destino también ha aprobado la moción de enlace.

![Estado de Enlace de la Puerta de Enlace](./gateway-link-status.png)

Mientras que una sola puerta de enlace puede tener múltiples solicitudes de enlace entrantes de otras puertas de enlace, cada puerta de enlace solo puede estar vinculada a una sola puerta de enlace.

Es posible desvincular una puerta de enlace con la moción correspondiente.

## Combustible de la puerta de enlace

Las puertas de enlace requieren Combustible Vórtice para cada salto. El combustible es proporcionado por contratistas que son designados por el gobierno.

![Moción de Combustible de la Puerta de Enlace](./gateway-fuel-motion.png)

De manera similar a la moción general de mantenimiento de infraestructura, los contratistas de combustible pueden ser designados para varias fases de mantenimiento. Las fases se alinean con las fases de mantenimiento. Es posible tener múltiples contratistas para la misma fase. El objetivo de nivel de servicio define el número mínimo de saltos exitosos de todos los intentos realizados. Los contratistas de combustible tienen acceso al almacén de Combustible Vórtice de la puerta de enlace.

## Tráfico de la puerta de enlace

El comando `GTWT` (tráfico de la puerta de enlace) muestra información relacionada con el tráfico de la puerta de enlace y la disponibilidad de combustible. Tiene una tabla que muestra los saltos en las últimas 24 horas, la capacidad actual, el combustible disponible y los contratistas de combustible. Una tabla también lista los saltos salientes y entrantes en la fase actual, la anterior y las últimas 10 fases. Los saltos salientes se desglosan además en intentos de salto exitosos y fallidos. Las razones de los saltos fallidos incluyen: fallido debido a que la puerta de enlace está inoperable. Este es el caso cuando el mantenimiento semanal no se paga a tiempo. Otras razones son: fallido debido a la falta de combustible y fallido debido a estar sobre la capacidad.

![Tráfico de la Puerta de Enlace](./gateway-traffic.png)

## Vuelos de la puerta de enlace

Las puertas de enlace están incorporadas en el comando `SFC` (controles de vuelo de la nave). Es posible planificar un vuelo como de costumbre, y el sistema utilizará las puertas de enlace en consecuencia. Es posible desactivar el uso de puertas de enlace en las preferencias de ruta. `SFC` mostrará el costo asociado con un salto de puerta de enlace.

Usar una puerta de enlace agrega tres segmentos de vuelo al vuelo: `LOCK`, `GTW` y `DCAY`. Durante el segmento `LOCK`, la nave espera a que la puerta de enlace se prepare para el salto. El pago de la tarifa de la puerta de enlace ocurre aquí. `GTW` es el salto real. Tenga en cuenta que esto no requiere ningún combustible FTL propio de la nave. `DCAY` ocurre justo en la puerta de enlace de destino después del salto. Una vez que la nave esté segura para continuar su viaje, comienza el siguiente segmento.

Aquí hay un ejemplo de vuelo de Umbra a LS-300c utilizando dos saltos de puerta de enlace separados.

![Vuelos de la Puerta de Enlace](./gateway-sfc.png)

Si una puerta de enlace está inoperable debido a la falta de materiales de mantenimiento, no es posible planificar un vuelo utilizando esa puerta de enlace. Los saltos de puerta de enlace pueden fallar por varias razones:

* La puerta de enlace se volvió inoperable después de que se envió el plan de vuelo
* Fondos insuficientes para cubrir la tarifa de la puerta de enlace
* Combustible Vórtice insuficiente para proceder con el salto
* La puerta de enlace eliminó o cambió el enlace a otra puerta de enlace después de que se envió el plan de vuelo

En todos estos casos, el operador de la nave recibirá una notificación y el vuelo terminará automáticamente en la puerta de enlace.

Las conexiones de las puertas de enlace se mostrarán como líneas rosas en el mapa. Una línea sólida significa que ambas puertas de enlace están operativas y los vuelos en ambas direcciones son posibles. Si la línea tiene pequeñas flechas, los vuelos solo pueden ocurrir en la dirección indicada. Las líneas discontinuas se muestran cuando ambas puertas de enlace están inoperables. Las conexiones que están `INCOMPLETAS` no se muestran.

![Conexiones de la Puerta de Enlace](./gateway-connections.png)
