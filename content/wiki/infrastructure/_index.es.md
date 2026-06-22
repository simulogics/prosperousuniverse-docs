---
title: "Infraestructura"
date: 2025-11-06T17:00:49+02:00
---

## Información general

Los proyectos de infraestructura son grandes proyectos planetarios que son iniciados por un gobierno planetario. Son construidos y operados por empresas individuales a través de contratos de contratista especializados ofrecidos por el gobierno.

Hasta ahora, el único tipo de infraestructura son las [puertas de enlace](../infrastructure-gateway).

La infraestructura de un planeta se puede consultar con los comandos `PLI` e `INF`. Tenga en cuenta que `INF` también muestra proyectos planetarios.

![Lista de Infraestructura](./infrastructure-list.png)

## Construcción de infraestructura

La infraestructura solo puede ser construida por un gobierno planetario. Hay una variedad de componentes de moción relacionados con la infraestructura, y el que se utiliza para construir cualquier infraestructura es "Construcción de infraestructura".

![Construcción de Infraestructura](./infrastructure-construction.png)

A continuación se describen los pasos típicos para construir una infraestructura.

Primero, se debe completar la moción de "Construcción de infraestructura". Esta moción especifica el pago que recibirá el constructor por sus servicios. También permite establecer una fecha límite hasta la cual la construcción debe finalizar. El constructor puede ser cualquier usuario.

![Moción de Construcción de Infraestructura](./infrastructure-construction-motion.png)

Una vez que la moción ha sido votada con éxito, se forma un nuevo contrato entre el gobierno y la empresa del constructor. El constructor puede elegir aceptar/cerrar el contrato o rechazarlo si lo recibió por error.

![Contrato de Construcción de Infraestructura](./infrastructure-construction-contract.png)

El contrato consta de tres partes. Primero, el pago del contratista. Segundo, una condición del contrato que inicia el proceso de construcción. Esta condición debe ser cumplida por el constructor. Una vez cumplida, el proyecto de infraestructura se inicia en la ubicación dada y se crea un almacén de construcción. Por último, una vez que todos los materiales de construcción se han entregado en el sitio de construcción, la última condición se cumple automáticamente y la infraestructura está completa.

![Almacén de Construcción de Infraestructura](./infrastructure-construction-store.png)

Tenga en cuenta que todas las infraestructuras que se encuentran en órbita tienen sus propias direcciones. Esto significa que volar a la órbita de un planeta no es suficiente para transferir materiales de construcción, por ejemplo. Las naves deben ser dirigidas a la infraestructura específica o al sitio de construcción.  

## Gestión de infraestructura

La mayoría de las infraestructuras requieren mantenimiento semanal para estar operativas. El comando `INFU` (mantenimiento de infraestructura) proporciona una visión general de toda la información relacionada con el mantenimiento.

![Mantenimiento de Infraestructura](./infrastructure-upkeep.png)

Muestra qué materiales y cuántos se requieren por fase de mantenimiento semanal, información sobre la fase de mantenimiento actual y un historial de las últimas fases de mantenimiento.

El estado operativo de la infraestructura cambiará de "mantenimiento faltante" a "operativa" una vez que todos los materiales requeridos se hayan transferido al almacén de mantenimiento. El almacén de mantenimiento puede contener materiales de mantenimiento para tres fases de mantenimiento. Para acceder al almacén de mantenimiento, se debe designar un contratista mediante una moción. Solo estos contratistas pueden acceder al almacén de mantenimiento.

![Moción de Mantenimiento de Infraestructura](./infrastructure-upkeep-motion.png)

En el editor de mociones se pueden seleccionar varios parámetros. Define la fase en la que debe comenzar el contrato de mantenimiento y durante cuántas fases debe ejecutarse. También permite especificar el contratista y el pago por fase. El objetivo de nivel de servicio define la proporción mínima de la infraestructura que debe estar operativa frente al estado de "mantenimiento faltante".

Por ejemplo, si el nivel de servicio se define en un 50% y el contratista proporciona los materiales de mantenimiento necesarios en el quinto día de la fase de mantenimiento, la condición del contrato se violará, ya que la infraestructura ha estado en estado de "mantenimiento faltante" durante aproximadamente el 71%.
 
Es posible tener múltiples contratistas para la misma fase de mantenimiento.

## Actualizaciones de infraestructura

Algunas infraestructuras pueden ser actualizadas. La selección de la moción depende del tipo de infraestructura. Aquí hay un ejemplo de una actualización de puerta de enlace:

![Moción de Actualización de Infraestructura](./infrastructure-upgrade.png)

Una vez que la moción se aprueba, se forma un contrato con el contratista especificado. Una vez que el contratista acepta el contrato, obtendrá acceso a un almacén de construcción, de manera similar al contrato de construcción de infraestructura.

La infraestructura permanece operativa durante el proceso de actualización.

## Nomenclatura de infraestructura

Es posible asignar un nombre a cualquier infraestructura. Nuevamente, esto es posible mediante una moción. No hay límite en la frecuencia con la que se puede cambiar el nombre de una infraestructura.

## Activos

El comando `ASTS` (Activos) proporciona una visión general de los proyectos de infraestructura en sus diversas etapas. Enumera los proyectos de infraestructura que están en construcción, la infraestructura propia (es decir, proyectos terminados) y los proyectos construidos. El comando está disponible en los contextos de la empresa y del gobierno, y su contenido se ajusta en consecuencia: una empresa nunca puede tener una entrada en la subsección "Propia", un gobierno no puede construir infraestructura directamente, por lo que la subsección "Construida" estará vacía.

El comando también mostrará enlaces útiles a los respectivos almacenes de construcción en la sección "En construcción". 

![Comando Activos](./assets.png)