---
title: "Reglas Locales"
date: 2024-06-27T07:26:49+02:00
---

## Información General

Las reglas locales son un conjunto de normas, tarifas e impuestos que se aplican en una ubicación determinada. El gobierno local puede
cambiar las reglas locales mediante mociones. Todos los ingresos provenientes de tarifas e impuestos se transfieren al gobierno. Las reglas locales se pueden
consultar con el comando `LR`. Aquí hay un ejemplo:

![Ejemplo de Reglas Locales](local_rules.png)

## Tarifas

### Tarifas del mercado local

La tarifa del mercado local se debe pagar al publicar un anuncio. Consiste en dos partes: la tarifa base y un componente de tiempo. El componente de tiempo aumenta linealmente con la duración del anuncio, es decir, cuánto tiempo estará visible en el mercado local.

Dependiendo de la ubicación del mercado local, los dos componentes tienen los siguientes límites:

| Tipo               | Parte Base | Parte de Tiempo |
|--------------------|-----------|----------------|
| Planeta inicial    | 50 - 150  | 3 - 8          |
| Planeta de facción | 25 - 200  | 2 - 10         |
| Planeta no perteneciente a una facción | 0 - 9_999 | 0 - 9_999 |

### Tarifas de producción

Las tarifas de producción deben pagarse una vez que se inicia una orden de producción. La altura real de la tarifa de producción para cualquier orden dada se determina una vez que la orden se agrega a la cola.

Las tarifas de producción se pueden definir para cada categoría de experiencia / tipo de fuerza laboral. La tarifa de producción se puede calcular construyendo la suma ponderada de todas las fuerzas laborales que se requieren para el edificio dado.

Dependiendo de la ubicación, las tarifas de producción tienen los siguientes límites:

| Tipo               | Tarifa de Producción |
|--------------------|--------------------|
| Planeta inicial    | 10 - 90            |
| Planeta de facción | 5 - 120            |
| Planeta no perteneciente a una facción | 0 - 9_999 |

#### Ejemplo

La producción de Polímero Granulado requiere una Planta de Polímero que emplea 10 pioneros y 25 colonos cuando está completamente equipada.
Supongamos que las tarifas de producción para los pioneros son 15 y las de los colonos 12. En total, la tarifa de producción será

(10 * 15 + 25 * 12) / (10 + 25) = 12.9

Dado que el Polímero Granulado solo tarda 8h24m en producirse, la tarifa de producción final es

12.9 * (8.5 / 24) = 4.56

### Tarifas de almacén

Las tarifas de almacén se deben pagar cada semana por cada unidad alquilada. Si no se puede pagar la tarifa de almacén debido a la falta de fondos, el inventario del almacén se bloquea y no está disponible para el usuario. Una vez que los fondos estén disponibles, las tarifas de almacén se pagan automáticamente y se desbloquea el inventario.

Dependiendo de la ubicación, las tarifas de almacén tienen los siguientes límites:

| Tipo               | Tarifa de Almacén |
|--------------------|------------------|
| Planeta inicial    | 100 - 2_500      |
| Planeta de facción | 75 - 5_000       |
| Planeta no perteneciente a una facción | 0 - 10_000 |

### Tarifas de establecimiento de base

Las tarifas de establecimiento de base son un costo opcional adicional al construir una base. Su propósito es ayudar al gobierno local a adaptarse al aumento de la demanda de materiales de mantenimiento de infraestructura y fuerza laboral debido a nuevas bases.

La primera base siempre está exenta de la tarifa de establecimiento de base.

Dependiendo de la ubicación, las tarifas tienen los siguientes límites:

| Tipo               | Tarifa de Establecimiento de Base |
|--------------------|----------------------------------|
| Planeta inicial    | 0 - 10_000                       |
| Planeta de facción | 0 - 20_000                       |
| Planeta no perteneciente a una facción | 0 - 10_000_000 |
