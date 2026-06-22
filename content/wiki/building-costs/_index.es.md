---
title: "Costos de Construcción"
date: 2018-09-18T17:13:49+02:00
---

Esta página enumera todas las reglas vigentes para los costos de construcción. Si deseas saber cómo configurar edificios, consulta la página de [Configuración de la base](../../tutorials/current-tutorials/02-first-base/index.html).

## Información general

Los costos básicos de construcción de cada edificio se pueden consultar en la ventana BSC de tu base (haz clic en “CONSTRUIR” en la vista general de tu base). Allí encontrarás un resumen de los costos de construcción de todos los edificios que se pueden construir en tu base.:

![Construct buffer](construct-buffer-pioneer-habitation.jpg)

Hacer clic en cualquiera de los símbolos de los edificios revelará su ventana BUI, que muestra sus costos de construcción:

![Habitation building costs](pioneer-habitation-details.jpg)


Sin embargo, esta información solo muestra una parte del panorama. Se refiere a _esta_ base en particular, que se encuentra en un planeta concreto. Los costos de construcción en otros planetas pueden variar según el conjunto de reglas que se detallan a continuación.

## Cálculo de costos

Cada edificio necesita una cierta configuración de Prefabricados de Construcción para ser construido. Además, se requerirán Materiales de Construcción y/o Partes de Construcción ("Recursos adicionales" a continuación) _una vez_ para _cada_ edificio, dependiendo de las condiciones ambientales. El número exacto de algunos recursos adicionales depende del costo de área de un edificio, que se indica en su ventana BUI (ver captura de pantalla arriba).

Ten en cuenta que todos estos costos adicionales también se aplican a los [proyectos planetarios](../../tutorials/planetary-projects) y [proyectos corporativos](../../tutorials/corporations/#corporate-actions-and-projects).

### Planetas rocosos

__Recurso adicional:__ Granulado de Construcción Mineral (MCG)  
__Cantidad:__ Área x 4

### Planetas gaseosos
__Recurso adicional:__ Fundación Aerostática (AEF)  
__Cantidad:__ Área / 3

### Presión atmosférica  

#### Baja presión (< 0.25 atm)

__Recurso adicional:__ Sellador de Polisulfito (SEA)  
__Cantidad:__ Área x 1

#### Alta presión (> 2.0 atm)

__Recurso adicional:__ Elementos Estructurales Endurecidos (HSE)  
__Cantidad:__ 1 por edificio

### Gravedad

#### Baja gravedad (< 0.25 g):

__Recurso adicional:__ Cobertura Magnética del Suelo (MGC)  
__Cantidad:__ 1 por edificio

#### Alta gravedad (> 2.5 g):

__Recurso adicional:__ Líquido Respirable de Alto Oxígeno (BL)  
__Cantidad:__ 1 por edificio  
_Ten en cuenta: Esta mercancía se encuentra en la categoría de Químicos, no en Materiales de Construcción._

### Temperatura

#### Baja temperatura (<-25° C):

__Recurso adicional:__ InsuFoam (INS)  
__Cantidad:__ Área x 10

#### Alta temperatura (> 75° C):

__Recurso adicional:__ Protección Térmica (TSH)  
__Cantidad:__ 1 por edificio

### Fertilidad
Las granjas y los huertos requieren un planeta con suelo fértil para ser construidos.

{{% about-this-page %}}
