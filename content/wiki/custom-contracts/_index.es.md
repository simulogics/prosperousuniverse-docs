---
title: "Contratos Personalizados"
date: 2022-07-25T10:30:49+02:00
---

## Información general

El comando `CONTD` permite la creación, edición y envío de borradores de contratos para crear contratos personalizados con otras partes. Los contratos personalizados se introdujeron con la versión **Convergence** y se agregaron tipos de borradores adicionales con la versión **Liquidity**.

## Lista de borradores de contratos

Abrir el comando `CONTD` sin ningún parámetro mostrará la lista de todos los borradores de contratos:

![lista de borradores de contratos](contd.png)

Es posible crear nuevos borradores, copiar borradores, eliminar borradores y abrir borradores existentes para editarlos.

## Editando un borrador de contrato

Un borrador de contrato tiene dos secciones, una para la información general y otra para las condiciones.

En la primera sección se puede nombrar el contrato. El nombre es privado y no será visible para la parte contratante. Su propósito es poder recordar para qué sirven los borradores de contratos específicos. El preámbulo del contrato es un campo de texto libre que se transmitirá una vez que el borrador se envíe a otra parte. El creador del contrato puede expresar sus intenciones con el contrato en forma de texto, en lugar de solo las condiciones del contrato.

La segunda sección trata sobre las condiciones del contrato. Hacer clic en el botón "seleccionar plantilla" abrirá una superposición que permite seleccionar una plantilla de borrador de contrato. Hay tres plantillas de contrato ("comprar mercancía", "vender mercancía", "enviar mercancía") que son similares a los anuncios disponibles en los mercados locales. Además de estas, también hay tres plantillas de contratos de préstamo.

Al igual que con los planos, cualquier cambio solo se guardará una vez que se presione el botón de guardar. Presionar 'DESCARTAR' restablecerá el borrador a su último estado.

Las condiciones individuales se pueden ajustar con el botón 'condición'. Dependiendo de la condición, una superposición permitirá cambiar materiales, ubicaciones, monedas, cantidades, etc. El botón 'parámetro' permite cambiar la fecha límite de una condición.

![borrador de contrato](contd2.png)

## Enviando un borrador de contrato

Un borrador de contrato se puede enviar a cualquier licenciatario. Enviar el contrato creará una copia del borrador de contrato y convertirá esa copia en un contrato regular. Será visible en la lista de contratos `CONTS` en estado abierto.

El destinatario recibe una notificación sobre el nuevo contrato y puede revisarlo. Un contrato puede luego ser cerrado o rechazado. En ambos casos, el remitente recibirá una notificación al respecto.

Realizar cambios en el borrador de contrato después de que se haya utilizado para crear un contrato no cambiará los contratos creados. Un borrador de contrato se puede usar varias veces.

Agregar a alguien a la lista de bloqueados evitará la recepción de borradores de contratos de ese licenciatario.

Enviar un borrador de contrato requiere una licencia `PRO`, cerrar uno requiere ya sea `BASIC` o `PRO`.

{{% about-this-page %}}
