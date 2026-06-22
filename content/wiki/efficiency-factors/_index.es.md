---
title: "Factores de eficiencia"
date: 2018-09-18T17:13:49+02:00
---

## Información general

Cada línea de producción opera a una cierta eficiencia cuando está activa. La eficiencia dicta cuánto tiempo tarda en completarse una orden de producción: una eficiencia más baja resulta en tiempos de producción más largos, mientras que una eficiencia más alta los acorta. La eficiencia actual de una línea de producción se puede consultar en su búfer de cola de producción (PRODQ):

![PRODQ](prodq.png)

La condición del edificio, la disponibilidad de trabajadores y la satisfacción proporcionan el valor base de eficiencia. Los expertos otorgan bonificaciones a ese valor para las líneas de producción en su campo de especialización. Los programas activos de CoGC también pueden beneficiar a ciertas industrias o tipos de trabajadores. Finalmente, la fertilidad del suelo (o la falta de ella) proporciona otra bonificación (o penalización) a la eficiencia de ciertas líneas de producción.

### Condición del edificio

Los edificios de producción son más eficientes justo después de la construcción, luego comienzan a deteriorarse. El deterioro aumenta lentamente con el tiempo hasta que el edificio opera al 33 % de su eficiencia original, momento en el cual deja de deteriorarse. Vale la pena señalar que todos los edificios pueden (y deben) ser reparados una vez que se consideran demasiado ineficientes.

### Disponibilidad de trabajadores

Cada línea de producción emplea una cierta cantidad y tipo de trabajadores, lo cual se indica en la sección "Fuerza laboral" de su ventana BUI:

![Fuerza laboral](workforces.png)

Si solo está disponible una parte de la fuerza laboral requerida, el edificio aún puede operar, pero a una eficiencia menor. Los edificios que requieren la misma fuerza laboral se suman.

Además del nivel de satisfacción (más sobre eso a continuación), la ventana de Población muestra tres métricas para cada tipo de trabajador:
1. Tamaño de la población: La cantidad real de trabajadores presentes en tu base. Determina la tasa a la que se consumen los recursos.  
2. Capacidad: La cantidad de trabajadores que tu base puede albergar actualmente.  
3. Requerido: La cantidad de trabajadores que todas tus líneas de producción combinadas pueden emplear.  

![Fuerza laboral total](total-workforce.png)

Se aplican las siguientes reglas:  
- Si la Capacidad es menor que la Requerida, la eficiencia de todas las líneas de producción que requieren el tipo de fuerza laboral respectivo se ve afectada negativamente. Más precisamente, la eficiencia se multiplica con el porcentaje de trabajadores disponibles, es decir: _Eficiencia x (Tamaño de la población / Requerido)_  
- Si la Capacidad es mayor que la Requerida, los Módulos de Habitación no se llenan completamente, lo que significa que el número real de trabajadores presentes – el Tamaño de la población – está por debajo de la Capacidad.  
- Todas las líneas de producción emplean trabajadores incluso cuando no hay pedidos en cola o la producción está detenida. Los trabajadores inactivos no pueden ser trasladados de un edificio a otro.  

### Satisfacción de los trabajadores

Cada tipo de trabajador tiene sus propias necesidades que deben cumplirse para mantener la eficiencia. Las necesidades de los trabajadores se pueden consultar en la ventana de Población de una base. Por ejemplo, 100 Pioneros necesitan 4 DW, 4 RAT, 0.5 OVE, 0.5 COF y 0.2 PWO por día para estar completamente satisfechos, y 100 Colonos necesitan 5 DW, 6 RAT, 3 HI, 0.5 EXO y 0.5 PT.

La eficiencia se mantiene al 100% si se cumplen tanto las necesidades de lujo como las no esenciales, y disminuye si solo se cumplen las necesidades esenciales. Por ejemplo, los Pioneros estarán al 79% de satisfacción si solo hay disponibles DW, RAT y OVE para consumir. Una fuerza laboral seguirá trabajando mientras al menos uno de sus recursos esenciales esté a su disposición. Solo cuando todos se agoten, la producción se detendrá. Si solo una parte de los recursos requeridos está disponible, la satisfacción de la fuerza laboral disminuye y, por lo tanto, su productividad se ve afectada.

Algunos consumibles son llamados no esenciales: La pérdida de productividad causada por la falta de un no esencial es menor que la de los consumibles esenciales. Además, una fuerza laboral dejará de trabajar por completo si el único consumible a su disposición es no esencial. El buffer de Población lista qué consumibles son esenciales y cuáles no:

![No esenciales](non-essentials.png)

#### Cómo se consumen los recursos

La primera cantidad completa de cualquier consumible requerido para las siguientes 24 horas (por ejemplo, 4 RAT para 100 Pioneros) es reclamada por la población de una base (y por lo tanto desaparece del inventario) tan pronto como el producto esté disponible en el inventario de la base. Lo mismo ocurre nuevamente 24 horas después, una y otra vez hasta que el consumible se agote. Esto se aplica a cada tipo de consumible individualmente: Si una población comienza a consumir DW a las 12 PM y RAT a las 4 PM, el siguiente lote de DW se consumirá a las 12 PM del día siguiente, y el siguiente lote de RAT se consumirá a las 4 PM del día siguiente.

__¡Nota: No es necesario que haya producción en funcionamiento para que una población consuma recursos!__ Las fuerzas laborales inactivas tienen las mismas necesidades que las activas y seguirán consumiendo los recursos del inventario de la base.

![Pioneros y Colonos](pioneers-and-settlers.png)

### Expertos

Todos los edificios pueden recibir bonificaciones de los llamados expertos. Puedes ver tus expertos presionando el botón EXPERTOS en tu base. Para utilizarlos, presiona ACT (Activar); para eliminar su bonificación, presiona RMV (Eliminar).

![Expertos](experts.png)

Cada experto otorga una bonificación a una industria específica. Cada industria, a su vez, abarca diferentes edificios:

| Especialización	   			| edificios (+ BUI tickers)														|
|-----------------------|-------------------------------------------------------------------			|
| Extracción de Recursos	| Collector (COL), Extractor (EXT),	Rig (RIG), Incinerator (INC)				|
| Manufactura  		| Basic Materials Plant (BMP), Textile Manufacturing (CLF), 3D Printer (PPF), Weaving Plant (WPL), Medium Component Assembly (MCA), Small Components Assembly (SCA), Spacecraft Prefab Plant (SPP), Appliances Factory (APF), Advanced Appliances Factory (AAF), Spacecraft Propulsion Factory (SPF)	|
| Agricultura  			| Farmstead (FRM), Hydroponics Farm (HYF), Orchard (ORC)        				|
| Industrias Alimentarias		| Food Processor (FP), Fermenter (FER), In-Vitro Plant (IVP)                     |
| Construcción			| Prefab Plant MK1 (PP1), Welding Plant (WEL), Prefab Plant MK2 (PP2), Unit Prefab Plant (UPF), Prefab Plant MK3 (PP3), Prefab Plant MK4 (PP4) |
| Metalurgia			| Smelter (SME), Metalist Studio (FS), Glass Furnace (GF), Hull Welding Plant (HWP), Ship Kit Factory (SKF), High-Power Blast Furnace (ASM) |
| Química				| Chemical Plant (CHP), Polymer Plant (POL), Laboratory (LAB), Pharma Factory (PHF), Technetium Processing (TNP), Advanced Material Lab (AML), Einsteinium Enrichment (EEP) |
| Refinación de Combustible			| Refinery (REF) |
| Electrónica			| Electronic Device Manufactory (EDM), Cleanroom (CLR), Energy Component Assembly (ECA), Electronics Plant (ELP), Software Development (SD), Drone Shop (DRS), Software Labs (SL) |


#### Tasas de aparición y bonificaciones de expertos

Los primeros expertos de cualquier empresa están incluidos en su [paquete inicial](../packages-factions), pero todos los expertos siguientes aparecerán con el tiempo. __Mantener una línea de producción en funcionamiento__ eventualmente creará un nuevo experto en su campo, por ejemplo, producir bienes con un Farmstead generará expertos en Agricultura con el tiempo. Después de alcanzar un total de 5 expertos en una industria en particular, no se crearán nuevos expertos en esa industria. Un total de 5 expertos pueden estar activos _por industria_ y un total de 6 expertos a la vez pueden estar activos en _todas las industrias_ en una base.

| Experto no.	| Días requeridos | Bonificación		   |
|---------------|---------------|--------------|
| 1			   	| 10.00 		| 3.06%	   	   |
| 2			   	| 12.50		   	| 6.96%	 	   |
| 3			   	| 57.57		   	| 12.48%	   |
| 4			   	| 276.50	   	| 19.74%	   |
| 5			   	| 915.10	   	| 28.40%	   |

Los días indicados arriba se refieren a un solo edificio al 100% de eficiencia. Operar dos edificios en la misma industria, es decir, dentro de la misma categoría de especialización, reducirá el tiempo requerido a la mitad, operar tres lo reducirá a un tercio, etc. Esto también ocurre cuando ambos edificios forman parte de la misma línea de producción, por ejemplo, dos (tres, cuatro, cinco...) Farmsteads reducirán el tiempo de manera equivalente.

Tenga en cuenta que la acumulación de **Días Requeridos** se reinicia después de cada experto. Por lo tanto, pasar de 0 a 2 expertos tomará 22.50 días.

La bonificación otorgada por un experto es un valor fijo que se multiplica simplemente con la eficiencia de la fuerza laboral. Por ejemplo, una fuerza laboral que opera al 90% de eficiencia operará al 101.2% de eficiencia una vez que se activen 3 expertos en la base. `90% * (100% + 12.48%) = 101.2%`

### Fertilidad del suelo

La eficiencia de ciertos edificios se ve afectada por la fertilidad del suelo de un planeta. Si este es el caso, se indicará junto a la entrada del edificio en la ventana BSC. Los edificios que actualmente requieren suelo fértil son Farmstead (FRM) y Orchard (ORC).

![Fertile soil](fertile-soil.png)

La fertilidad del suelo de un planeta se puede ver en su ventana PLI. Cuanto más a la derecha llegue la parte amarilla de la barra, más fértil es; cuanto más a la izquierda llegue, menor será el valor de fertilidad. __Nota: Si hay dos guiones en lugar de una barra, el planeta es infértil, lo que significa que los edificios afectados por la fertilidad del suelo no pueden operar en absoluto aquí.__

![Fertilidad del suelo](soil-fertility.png)

La fertilidad neutral (es decir, sin amarillo) indica un modificador de +0%. La fertilidad pobre (amarillo a la izquierda del centro) es un modificador negativo, mientras que la fertilidad alta (amarillo a la derecha del centro) es un modificador positivo. Cuanto más se extienda la barra amarilla, mayor será su impacto, con un rango máximo de aproximadamente -33% a +33%.

### Programas CoGC

La [Cámara de Comercio Global](../../tutorials/planetary-projects#chamber-of-global-commerce-cogc), si existe en un planeta y está activa, puede proporcionar un bono temporal a la productividad. Al igual que con los expertos, el porcentaje respectivo se suma simplemente encima. Por ejemplo, el programa CoGC _Eventos Educativos: Pioneros_ proporciona un bono del 10 % a todos los edificios operados por pioneros mientras esté activo, y el programa _Campaña Publicitaria: Agricultura_ otorga un bono del 25 % a todas las instalaciones del sector agrícola.

{{% about-this-page %}}
