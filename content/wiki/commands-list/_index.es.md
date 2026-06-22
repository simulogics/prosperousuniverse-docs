---
title: "Lista de Comandos"
date: 2018-09-18T17:13:49+02:00
---

Esta es una lista completa de todos los comandos disponibles para ti en APEX. Están agrupados por sus respectivas áreas de uso. Comprender esta lista requiere que ya estés familiarizado con [cómo funcionan los comandos](../../tutorials/legacy-tutorials/commands). Puedes leer toda la lista para obtener una visión general o usarla como referencia para buscar comandos específicos.

## Comandos de base

__BS__  
_Parámetro opcional: ID de la base_  
Por sí solo muestra una visión general de todas tus bases. Muestra más información sobre una base concreta cuando se sigue de un ID de base, por ejemplo, al hacer clic en "Ver Base" en la ventana genérica de BS. Proporciona acceso a la mayoría de los demás comandos relacionados con la base.

__BSC__  
_Parámetro obligatorio: ID del planeta_  
Permite crear una nueva base en un planeta. Muestra los materiales de construcción necesarios y permite seleccionar un terreno en la superficie. 

__BSL__  
_Parámetro obligatorio: ID de la base_  
Muestra una visión general de los edificios en una base concreta. Accesible a través del botón EDIFICIOS (anteriormente "SECCIONES") en una ventana concreta de BS. Haz clic en "DEMOLER" para destruir una Sección, lo que reembolsará algunos de los recursos que se utilizaron en su construcción, dependiendo de su antigüedad. Los materiales posibles de reembolso se enumeran como "Materiales recuperables".

__BSC__  
_Parámetro obligatorio: ID de la base_  
Abre la ventana de Construcción de una base concreta. Accesible a través del botón "Construir" en una ventana concreta de BS. Usa las pestañas en la parte superior para recorrer diferentes categorías de edificios. La línea etiquetada como "Área" indica el costo de área de un edificio y, después de la barra, el área disponible restante en tu base. La línea etiquetada como "Fuerza laboral" muestra el número y tipo de trabajadores necesarios para operar este edificio.

__BUI__  
_Parámetro obligatorio: ticker del edificio_  
Muestra información sobre un tipo de edificio: qué tipo de trabajador se emplea aquí, cuánto espacio ocupa el edificio y qué partes se utilizan en su construcción. Accesible haciendo clic en un tipo de edificio en la ventana BSC.

__INV__  
_Parámetro opcional: dirección o ID de la tienda_  
Si no se proporcionan parámetros, el comando mostrará una lista de todos tus inventarios, incluyendo almacenamiento en la base, bodegas de carga, tanques de combustible y unidades de almacenamiento en almacenes. Al hacer clic en el botón "abrir" se mostrarán los contenidos del inventario seleccionado. En la parte superior izquierda, encontrarás varias opciones de clasificación (AMT: cantidad, WGT: peso, VOL: volumen) así como un símbolo a su izquierda. Haz clic en él para alternar entre el modo de lista y el modo de cuadrícula; este último muestra más información sobre cada mercancía, como su peso, volumen y valor contable.

Si el parámetro contiene una dirección de sistema o planeta (por ejemplo `INV XK-745` o `INV XK-745a`), solo se mostrarán los inventarios en esa ubicación.

__MTRA__  
_Parámetro opcional: ticker del material_  
_Parámetro opcional: ID de la tienda de origen_  
_Parámetro opcional: ID de la tienda de destino_  
Permite transferir una cantidad específica de artículos entre dos inventarios. El material a transferir, así como las tiendas de origen y destino, se pueden especificar mediante los parámetros del comando o elegir en los menús desplegables de la ventana del comando. Ten en cuenta que este comando también es accesible (con los detalles de transferencia prellenados) arrastrando un artículo desde la tienda de origen a la tienda de destino y soltándolo en la ranura "AMT".

__WF__  
_Parámetro obligatorio: ID de la base_  
Muestra una visión general de la fuerza laboral de una base y sus necesidades. Cuanto más sofisticado sea el nivel de la fuerza laboral, mayores serán sus necesidades. Si no puedes suministrar a tus trabajadores los consumibles que necesitan, la eficiencia de los edificios que operan disminuirá. Accesible a través del botón "Fuerza laboral" en una ventana concreta de BS.

__EXP__  
_Parámetro obligatorio: ID de la base_  
Muestra todos los campos que pueden recibir bonificaciones de los Expertos y muestra qué Expertos están siendo utilizados actualmente en la base especificada. Haz clic en “REMOVE” para desactivar un experto, que luego se listará como disponible en la columna más a la derecha. Haz clic en “ACT” para enviarlos de nuevo a trabajar. Accesible a través del botón "Expertos" en una ventana concreta de BS.
Comandos de línea de producción

__PROD__  
_Parámetro obligatorio: ID de la base_  
Muestra las Líneas de Producción en una base específica. Accesible a través del botón "Producción" en una ventana concreta de BS. Cada Línea de Producción puede consistir en uno o más edificios del mismo tipo.

__PRODQ__  
_Parámetro obligatorio: ID de la línea de producción_  
Permite cancelar órdenes en cola, pero no las que ya están siendo procesadas. El valor de eficiencia se ve influenciado por múltiples factores, incluyendo la satisfacción de tus trabajadores, el bono proporcionado por los Expertos y, en algunos casos, la fertilidad del suelo del planeta. Accesible a través del botón "Detalles" en una ventana de PROD.

__PRODCO__  
_Parámetro obligatorio: ID de la línea de producción_  
Permite colocar una nueva orden de producción. Selecciona un Producto Primario del menú desplegable, establece un tamaño de orden y coloca tu orden en la cola. Si tu orden requiere materiales de entrada (como se muestra en la parte inferior), asegúrate de que estén disponibles primero. Accesible a través del botón "Nueva Orden" en una ventana de PROD.

__HQ__  
_No possible parameter_  
Muestra cuál de tus bases es actualmente la sede de tu empresa y te permite trasladar tu sede a otra base para obtener diferentes [bonos de facción](../headquarters). También puedes mejorar tu sede aquí para desbloquear permisos de base adicionales y ranuras de cola de producción.

__BRA__  
_Parámetro opcional: ID del planeta_
Permite seleccionar una de tus bases y reparar múltiples de sus edificios a la vez especificando una condición mínima de los edificios. Todos los edificios en la base seleccionada que estén en o por debajo de esa condición se incluirán en las reparaciones.

__UPCK__
_Parámetro obligatorio: ID de la tienda_  
Muestra una lista de todos los paquetes de consumibles en la tienda seleccionada. Permite desempaquetar uno o más paquetes. Los paquetes siempre se desempaquetan en la misma tienda en la que se encuentran actualmente.

## Comandos sociales

__FA__  
_Parámetro obligatorio: código de facción_  
Muestra información sobre la facción especificada.

__CO__  
_Parámetro obligatorio: código de la empresa_  
Muestra información sobre la empresa especificada. (Aquí es donde se utiliza el código de cuatro dígitos que elegiste para tu empresa al principio.) Entre otras cosas, permite ver y contactar al propietario de la empresa.

__USR__  
_Parámetro obligatorio: nombre de usuario_  
Muestra la empresa de un usuario, la fecha de registro y el estado de conexión. Accesible a través de la columna “Managing Director” en una ventana de CO. Hacer clic en el botón “MUTE USER” hace que todos los mensajes enviados por este usuario sean invisibles para ti.

__COM__  
_No possible parameters_  
Lista todos los canales de comunicación a los que te has unido en el pasado. Te unes automáticamente a un canal cuando haces clic en él por primera vez. Para salir de un canal, ábrelo y selecciona “LEAVE”.

__COMC__  
_No possible parameters_  
Lista todos los canales de comunicación públicos. Puedes unirte a un canal seleccionándolo de la lista.

__COMG__  
_Parámetro obligatorio: ID del canal_  
Abre un chat grupal privado. Si previamente te uniste, ingresar su nombre abrirá el chat directamente. Si ingresas el nombre de una sala que aún no existe o a la que no te has unido previamente, “Iniciar conversación” abrirá el chat. También accesible a través del botón “NUEVO GRUPO” en la ventana COM.

__COMP__  
_Parámetro obligatorio: ID del canal_  
Abre un chat público existente como “global” o “help”. No puedes crear un nuevo chat público.

__COMU__  
_Parámetro obligatorio: nombre de usuario_  
Inicia una conversación privada de dos personas con el usuario especificado. Comienza a escribir su nombre hasta que aparezca en la lista, luego haz clic en él. Accesible a través del botón “NUEVO PRIVADO” en la ventana COM.

__CONS__  
_No possible parameters_  
Muestra quién está actualmente en línea en APEX. Accesible a través del botón “CONS” en la esquina inferior derecha de APEX.

## Comandos de contrato

__CONT__  
_Parámetro obligatorio: ID del contrato_  
Este comando te permite ver un contrato específico. Debe ir seguido de un parámetro largo y complejo que identifica el contrato, por lo que generalmente se recomienda usar el comando “CONTS” y luego hacer clic en el/los contrato(s) deseado(s).

__CONTS__  
_No possible parameter_  
Muestra una lista de todos tus contratos de los Mercados de Materias Primas y Mercados Locales. Haz clic en cualquier contrato para abrir su buffer CONT. Ten en cuenta que también puedes ver los Contratos Pendientes seleccionándolos de la lista en la barra lateral derecha. (Si no puedes ver la barra lateral, actívala usando el botón SDBR a la izquierda.) Aprende más sobre contratos en los tutoriales “Trading” y “Mercados Locales”.

__CONTD__
_Parámetro opcional: ID del contrato_
Muestra una lista de todos tus borradores de contrato. Especificar un ID de contrato, o hacer clic en cualquier borrador, abrirá la vista de detalle del borrador, donde se puede editar y enviar.

## Comandos de intercambio de materias primas
Estos comandos se refieren a los intercambios de materias primas. Los dos primeros son probablemente los más útiles. Ve todos estos comandos en acción en el tutorial "Primeros pasos".

__CXOS__  
_No possible parameter_  
Muestra un historial de tus órdenes de venta y compra, que puedes ver y eliminar desde aquí. Al eliminar una orden que aún no se ha completado, o al menos no completamente, la retiras del mercado.

__CXO__  
_Parámetro obligatorio: ID del contrato_  
Muestra información sobre una orden que realizaste en el pasado. Accesible a través de los botones “VER” en la ventana CXOS.

__CXL__  
_No possible parameter_  
Lista todos los intercambios de materias primas existentes. Desde aquí, puedes acceder rápidamente a un intercambio de materias primas concreto sin tener que recordar su parámetro particular para el comando CX.

__CXM__  
_Parámetro obligatorio: ticker del material_  
_Parámetro opcional: ID del planeta_  
Compara la información del intercambio de materias primas para el material especificado en _todos_ los intercambios de materias primas. Los intercambios se ordenarán según su distancia al planeta dado (si se ingresó uno).

__CX__  
_Parámetro obligatorio: ID del intercambio de materias primas_  
Aquí es donde puedes comprar y vender artículos de un mercado en particular. Selecciona la categoría de materias primas del menú desplegable. Accesible, por ejemplo, haciendo clic en el nombre de un intercambio de materias primas en la ventana CXL.

__MAT__  
_Parámetro obligatorio: ID del material_  
Los materiales y las materias primas son esencialmente lo mismo. Su ticker es el identificador de dos o tres letras que puedes ver en cada uno de sus pequeños íconos. Por ejemplo, el ticker del acero es STL. "Producto trabajado" indica lo que se puede hacer con este material y en qué línea de producción, mientras que "Producción" muestra cómo y dónde se puede producir el material en sí. Accesible, por ejemplo, haciendo clic en el ícono de una materia prima en la ventana CX.

__CXP, CXPC, CXOB, CXPO__  
_Parámetro obligatorio: ID de la materia prima + ID del intercambio_  
Estos cuatro comandos se refieren a materias primas concretas en un mercado concreto. Junto a una entrada de una materia prima en la ventana CX, encontrarás los botones etiquetados como "INFO", "CHART", "ORDERS" y "TRADE".
"INFO": CXP, que muestra una visión general de las ofertas actuales, cantidades solicitadas, máximos y mínimos históricos, etc.
"CHART": CXPC. Muestra un gráfico de velas del precio de una materia prima a lo largo del tiempo. Si dice "No data", la materia prima no se ha vendido en el período de tiempo indicado. Selecciona una ventana de tiempo más larga para solucionarlo.
"ORDERS": CXOB, donde puedes ver las solicitudes y ofertas pendientes.
"TRADE": CXPO, que te permite realizar órdenes de compra y venta dentro del rango de precios actual. Este último se determina mediante un promedio de tres días y es más amplio para los licenciatarios PRO que para los licenciatarios FREE. Para establecer rápidamente la oferta más baja o el precio de venta actual, utiliza los botones "set" en la línea "Ask / Bid". La línea "Inventory" te permite seleccionar la ubicación de almacenamiento desde la cual vender tus materias primas.

## Comandos de vuelo espacial
Se recomienda utilizar el comando FLT y acceder a los demás comandos desde allí. Para ver todos estos comandos en acción, echa un vistazo al tutorial de vuelo espacial.

__FLT__  
_Parámetro opcional: ID del sistema / ID del planeta_  
Ingresado por sí solo, el comando Fleet muestra todas tus naves. Cada línea muestra datos sobre una de tus naves, como su código de transpondedor, nombre, estado, estado de llenado, ubicación e información sobre un vuelo en curso. Al seguir el comando de la flota con el ID de un sistema o planeta, se muestran todas tus naves actualmente estacionadas allí. (El ID es simplemente el parámetro que puedes ver en la parte superior de un búfer al seleccionar un sistema en el Mapa del Universo o un planeta en un mapa del sistema.)

__SHP__  
_Parámetro obligatorio: código de transpondedor de la nave_  
Muestra información sobre una de tus naves. Cambia el nombre de tu nave haciendo clic en su nombre actual (o "sin nombre") e ingresando uno nuevo.
Accesible haciendo clic en el código de transpondedor de una nave en la ventana FLT.

__SHPF__  
_Parámetro obligatorio: código de transpondedor de la nave_  
Muestra el estado del combustible de una nave. Accesible haciendo clic en la barra de combustible de una nave en la ventana FLT.

__SHPI__  
_Parámetro obligatorio: código de transpondedor de la nave_  
Muestra el inventario de una nave, que está limitado por el peso y el volumen de su carga. Accesible haciendo clic en la barra de inventario de una nave en la ventana FLT.

__SFC__  
_Parámetro obligatorio: código de transpondedor de la nave_  
El botón "FLY" junto a cada nave en la lista FLT llama al comando SFC seguido del código de transpondedor de la nave. Al ingresar un ID de planeta o estación en la propiedad Ubicación, configurar el uso de combustible deseado y presionar Iniciar, puedes enviar una nave a un nuevo destino.

__SI__  
_Parámetro obligatorio: código de transpondedor de la nave_  
Muestra toda la información pública disponible sobre la nave seleccionada. Accesible haciendo clic en un triángulo de nave en un mapa del sistema o en la ventana de información del planeta.

## Comandos de construcción de naves

__BLU__
_Parámetro opcional: ID del plano_
Abre una lista de todos tus planos de naves o un plano específico si se especificó un ID.

__SHY__
_Parámetro obligatorio: ID del planeta_
Abre el búfer del astillero del planeta deseado.

__SHYP__
_Parámetro obligatorio: ID del proyecto_
Abre el proyecto de construcción de naves deseado.

## Comandos de intercambio extranjero
Para ver estos comandos en acción, echa un vistazo al tutorial de "Intercambio Extranjero".

__FX__  
_No hay parámetros posibles_  
FX te muestra una matriz de tipos de cambio donde puedes ver cuánto vale una moneda en términos de otra. Las monedas base se disponen verticalmente, las monedas cotizadas horizontalmente.

__FXP__  
_Parámetro obligatorio: ticker del par de divisas_  
Usa FXP seguido de un ticker de dos identificadores de divisas separados por una barra o un punto, por ejemplo: FXP AIC/CIS. Alternativamente, simplemente haz clic en el valor respectivo en la matriz FX.

__FXOB__  
_Parámetro obligatorio: ticker del par de divisas_  
Usa este comando para ver las órdenes abiertas de cualquier par de divisas, por ejemplo: FXOB AIC/CIS.

__FXPC__  
_Parámetro obligatorio: ticker del par de divisas_  
Muestra el historial de tipos de cambio de cualquier par de divisas, por ejemplo: FXPC AIC/CIS.

__FXPO__  
_Parámetro obligatorio: ticker del par de divisas_  
Usa este comando para colocar una orden de intercambio extranjero, es decir, para gastar una moneda y comprar otra. Ingresa FXPO seguido del ticker deseado, por ejemplo: AIC/NCC. Luego, selecciona la pestaña correspondiente para comprar o vender la moneda deseada. Ten en cuenta que los números que indiques son Lotes, es decir, 1000 de cada moneda. Para obtener información más detallada, consulta el [tutorial de Intercambio Extranjero](../../tutorials/foreign-exchange).

__FXOS__  
_No hay parámetros posibles_  
Muestra todas las órdenes de intercambio extranjero que has colocado.

## Comandos de mapas
Los mapas se pueden navegar arrastrando y soltando el botón izquierdo del ratón para moverse y el botón derecho para rotar. Algunos mapas se pueden mostrar en 2D en lugar de 3D activando la propiedad "Fix 2D".

__MU__  
_Parámetro obligatorio: CX/NAV/INV/POL_  
Abre uno de los cuatro mapas diferentes del Universo. Todos muestran el mismo Universo, pero sirven para diferentes propósitos, como se describe a continuación. Los puntos interconectados en el mapa son sistemas estelares. Al pasar el cursor sobre un sistema, puedes ver su identificador. En todos los mapas, puedes alternar la visualización de diferentes tipos de información en la parte inferior. También puedes filtrar esos datos por período de tiempo (por ejemplo, 1 hora, 12 horas, 24 horas).

MU CX: Muestra dónde se están llevando a cabo tus intercambios de commodities.

MU NAV: Muestra datos de tráfico. Mientras “fleet” esté activado, las ubicaciones de tus naves se marcan con flechas amarillas. Aprende más sobre los datos de tráfico en el tutorial “Space Flight”.

MU INV: Permite ver la distribución de tu almacenamiento en el universo. Esto aún no está disponible.

MU POL: Muestra un mapa político. Esto aún no está disponible.

__MS__  
_Parámetro obligatorio: ID del sistema_  
Al igual que en el Mapa del Universo, las flechas amarillas marcan tus naves. Activa “tráfico” para ver también la ubicación de las naves de otros usuarios, que se marcan con flechas blancas. La estructura de alambre en el medio es la estrella del sistema; los círculos que la orbitan son planetas rocosos (blancos) o gaseosos (naranjas). Los cuadrados blancos representan estaciones espaciales. Al pasar el cursor sobre un planeta o estación espacial, se muestra su ID. En lugar de ingresar manualmente el ID del sistema, puedes hacer clic en el sistema deseado en el mapa del Universo.

__SYSI__
_Parámetro opcional: ID del sistema_
Todos los sistemas, nombrados o no, tienen un ID que consiste en el ID del sector (dos letras) y el número del sistema. El comando de información del sistema muestra información básica sobre el sistema, como su nombre, tipo de estrella, densidad de micrometeoritos y afinidad de facción. Tiene una lista de todos los planetas y estaciones en ese sistema.
Si no se proporciona un ID de sistema, se muestra un cuadro de búsqueda en lugar de los datos del sistema, lo que permite buscar sistemas.

__PLI__
_Parámetro opcional: ID del planeta_
Todos los planetas, nombrados o no, tienen un ID, que es el ID del sistema seguido de una letra única. La información del planeta contiene accesos directos a tu flota y almacenamiento en ese planeta. Entre otras cosas, puedes ver aquí qué recursos se pueden extraer de este planeta y su atmósfera, y si el planeta es adecuado para el cultivo de plantas. La barra que indica esto comienza en el medio, y cuanto más se extienda hacia la izquierda o derecha, más infértil o fértil es el planeta, respectivamente. Finalmente, el Tipo y la Temperatura indican si necesitarás [materiales de construcción adicionales](../building-costs) para establecer una base en este planeta.
Cada parcela no gris en un planeta se puede hacer clic para obtener más información sobre ella. Los siguientes colores existen hasta ahora: azul (otras empresas), azul oscuro (proyecto de otra corporación), amarillo (propia empresa), amarillo oscuro (proyecto de propia corporación), verde (CoGC), rojo (intercambio de productos básicos)
En lugar de ingresar el ID del planeta manualmente, también puedes hacer clic directamente en el planeta en el mapa del sistema para acceder a su ventana PLI.
Si no se proporciona un ID de planeta, se muestra un cuadro de búsqueda en lugar de los datos del planeta, lo que permite buscar planetas.

__STI__  
_Parámetro obligatorio: ID de la estación_  
Muestra información general sobre una estación espacial y proporciona acceso a su infraestructura. Accesible haciendo clic en una estación (símbolo cuadrado) en un mapa del sistema o en una ventana de información del planeta.

## Comandos de proyectos planetarios

__PPS__  
_Parámetro obligatorio: ID del planeta_  
Muestra todos los proyectos planetarios en el planeta deseado.

__PP__  
_Parámetro obligatorio: ID del planeta y del proyecto_  
Muestra información sobre un proyecto planetario concreto. Debido a la longitud y complejidad del parámetro, se recomienda acceder a esta información a través del botón “detalles” junto al proyecto deseado en el búfer PPS.

__PPI__
_Parámetro obligatorio: ID del planeta_  
Muestra información sobre una parcela en la superficie del planeta.

__POPR__
_Parámetro obligatorio: ID del planeta_   
Muestra los informes de población del planeta especificado con información sobre el tamaño de la población planetaria, la satisfacción de necesidades y el crecimiento.

### Comandos del Mercado Local

__LMOS__
_No possible parameter_  
Muestra todos tus anuncios del Mercado Local.

__LM__
_Parámetro obligatorio: ID del planeta_  
Muestra todos los anuncios disponibles en un Mercado Local determinado. Accesible haciendo clic en la entrada de infraestructura "Mercado Local" (si existe) en cualquier ventana PLI.

__LMA__
_Parámetro obligatorio: ID del anuncio_  
Muestra los detalles del anuncio del Mercado Local especificado. Accesible seleccionando un anuncio en la ventana LM.

__LMP__
_Parámetro obligatorio: ID del planeta_  
Permite colocar un anuncio de compra o venta en un Mercado Local determinado. Accesible a través del botón “PUBLICAR ANUNCIO” en una ventana LM.

### Comandos políticos

__ADM__
_Parámetro obligatorio: ID del planeta_  
Muestra información sobre el [Centro de Administración](../../tutorials/planetary-projects/#administration-center) del planeta (si existe), como el Gobernador actual, la entidad (es decir, Facción o Corporación) que recauda impuestos y tasas, y todos los candidatos para el próximo mandato. Permite a cualquier persona postularse para Gobernador del planeta y a los residentes planetarios votar por su candidato preferido.

__GOV__
_Parámetro obligatorio: ID del planeta_
Muestra información sobre los gobiernos actuales y anteriores de un planeta y las mociones que se votaron.

__LR__
_Parámetro obligatorio: ID del planeta_  
Muestra las Reglas Locales de un planeta, dado que tiene un Centro de Administración. Las Reglas Locales incluyen impuestos sobre la producción, así como tarifas para los anuncios del Mercado Local.

__MOT__
_Parámetros obligatorios: ID de administración, ID de moción_
Muestra una moción, incluidos sus componentes, estado actual y votos.

__MOTS__
_Parámetro opcional: ID de moción_
Muestra una lista de mociones para el contexto gubernamental actualmente activo.

__POL__
_Parámetro opcional: Nombre de usuario_
Muestra los cargos políticos actuales y pasados ocupados por un usuario, incluidos los cargos actuales.

### Comandos de almacén

__WAR__
_Parámetro obligatorio: ID del planeta_  
Muestra información sobre los almacenes públicos y privados, como la cantidad de unidades de almacenamiento disponibles, las tarifas de alquiler, etc.

## Comandos de notificaciones

__NOTS__
_No possible parameter_  
Muestra una lista de notificaciones dentro del juego. Haz clic en una notificación para obtener más información.

__NOTIG__
_No possible paramter_  
Permite cambiar la configuración de notificaciones dentro del juego. Los tipos de notificaciones deshabilitados no aparecerán en el comando `NOTS`.

__NOTPNS__
_No possible parameter_  
Permite cambiar la configuración de notificaciones push. Elige qué tipos de notificaciones deben enviarse por correo electrónico y con qué frecuencia.

## Comandos de transmisión

__TRA__  
_No possible parameter_  
Muestra una lista con todas las transmisiones, es decir, tutoriales en video.

__XIT__  
_Parámetro opcional: título_  
Muestra una pantalla verde para ayudarte a grabar tu propia transmisión. Usa el parámetro opcional para darle un título.

__XYTV__  
_Parámetro obligatorio: ID de YouTube_  
Incrusta un video de YouTube. El ID es la sucesión de números y letras después de “v=” en la URL del video.

## Otros comandos

__ARC__  
_No possible parameter_  
Muestra el estado actual de tu Centro de Representación APEX y te permite contribuir con fondos para aumentar su nivel.

__COLIQ__  
_No possible parameter_  
Permite liquidar tu empresa. Será desmantelada y podrás empezar de nuevo completamente con la misma cuenta. Actualiza APEX después de usarlo. Los siguientes tiempos de espera se aplican al comando COLIQ: El primer COLIQ estará disponible inmediatamente después de la creación de la empresa, el segundo 3 días después de usar el primero. El tiempo de espera para el tercer COLIQ es de 21 días, y cada tiempo de espera siguiente es de 60 días. Si no ha habido operaciones de productos básicos o del mercado local y no se han realizado contribuciones a proyectos planetarios o corporativos, podría ser posible un COLIQ inmediato. Ten en cuenta que el uso indebido del comando COLIQ puede resultar en la suspensión (temporal) de tu cuenta.

__CS__  
_No possible parameter_  
Permite crear una nueva Pantalla. Para llamar a este comando, puedes usar el botón “AGREGAR” en la parte superior. Aprende todo sobre las Pantallas en el tutorial de la interfaz APEX.

__FIN, FINLA, FINIS, FINBS__  
Estos cuatro comandos te proporcionan una visión detallada de la situación financiera de tu empresa. Más información sobre estos comandos se proporcionará próximamente.

__GIFT__
_No possible parameter_
Permite regalar tiempo de licencia PRO a otros jugadores y proporciona una visión general de los regalos enviados y recibidos.

__LEAD__  
_No possible parameter_  
Muestra las clasificaciones a nivel de empresa. El tipo de clasificación se puede elegir en un menú desplegable en la parte superior. Algunas clasificaciones admiten selectores adicionales (como especificar el rango de tiempo de los datos).

{{% about-this-page %}}