# La Migración: salvar el Mundo RU

Volver a experiencia [aquí](https://amadorsoy.github.io/proyectos/)

***


Mi cambio de _mago gris_ a **_mago blanco_** me vino como a **Gandalf** cuando tuve que salvar el mundo RU, me cambié a Repuestos Uruguay, S.A. a parte de por mejores condiciones, porque tenían un problema muy serio y si conseguía solucinarlo después iba a poder desarrollar otros _poderes_ como desarrollador que necesitaba afrontar para poder mejorar mis capacidades. Además, ya no tendría al angel de la guarda detrás para ayudarme o guiarme, a partir de ese momento mis decisiones harían que RU se salvara o no y eso también era un paso adelante en mi trayectoria profesional.

Lo que me encontré a mi llegada fue:

- 9 servidores de bases de datos distribuidos en las 8 tiendas y la central, con un sistema de replica que tenía su distribuidor y servidor principal en la central.

- Un sistema que tardaba aproximadamente 5 minutos en hacer una factura.

- En la central, cuando se hacía un pedido de compra, al hacer el cálculo sacaba a todos los usuarios del sistema porque lo _tumbaba_ literalmente.

- Un consumo por red de más de 100MB al abrir el software de Mostrador.

- Un Windows NT como controlador de Grupo, porque eso no se podía ni llamar dominio.

- Dos servidores descatalogados en la central cuyas fuentes de alimentación si caían ya no habían repuestos.

Así que había que salvar el **_Mundo RU_** y me puse a trabajar junto a dos compañeros de departamento, el primero no tocaba ni la base de datos ni el código fuente, pero tenía toda la experiencia de la empresa en su cabeza, por lo que nos resultaría de extrema ayuda para evitar perder cosas por el camino esenciales y para ayudarnos a llegar a buen puerto, además se encargaba de dar soporte a los usuarios y eso nos ahorraba mucho tiempo. El segundo compañero, empezó a cambiar la estructura de las tablas, que tenían lindeces como que las claves primarias eran decimales, no había ninguna [foreign key](https://es.wikipedia.org/wiki/Clave_for%C3%A1nea), etc. Ese ya era un gran paso para poder tener algo sobre el que empezar a hacer **La Migración**.

Todos los proyectos estaban en Delphi, en 3 versiones distintas, por lo que había que ponerse manos a la obra y tratar con todo el [Código Legacy](https://es.wikipedia.org/wiki/C%C3%B3digo_heredado). Me río de la [refactorización](https://es.wikipedia.org/wiki/Refactorizaci%C3%B3n) que hay que afrontar en algunos proyectos, tenía código de hace más de 20 años entre mis manos.

Fue trabajo de varios meses, tuvimos algún tropiezo que otro y aunque es cierto que la empresa tuvo paciencia, presionaba para que sacaramos todo para delante en el menor tiempo posible (a ser posible en dos o tres meses), algo que parecía imposible.

Hubo un gran escollo que no había podido contemplar de inicio por tener que cambiar cada campo de cada conexión a un tipo distinto en el código fuente de los programas. Resulta que habían tantos servidores de bases de datos como tiendas porque entre el código fuente del software y el código fuente de los procedimientos en la base de datos, llegaban a encontrarse hasta 3 y 4 [transacciones bloqueantes](https://es.wikipedia.org/wiki/Transacci%C3%B3n_(inform%C3%A1tica)) anidadas unas dentro de otras en procesos clave como realización de albaranes/facturas, cobrar facturas, etc.

Había que cambiar todo el código fuente en el que hubiera transacciones, tanto en software como en bases de datos, además había que arreglar una curiosa forma de crear los datos en las tablas que eran (cabecera-detalle), porque resulta que se creaba antes el detalle que la cabecera en casi todos los procesos (ahora ya saben porque no habían claves foráenas). Acabe creando mis propios procedimientos más arreglar los de las bases de datos y cambiando todo el código con **transacciones** que encontraba en los programas. 

Otra de las cosas que hice fue aprovechar para reducir el consumo de datos por red al iniciar y usar el software, cambie el software y de consumir más de 100MB pasó a consumir 3MB, estaba al nivel casi de una web.

Finalmente el **_Mundo RU_** se pudo salvar y acabó con solo dos servidores de bases de datos, un controlador de dominio con samba y todas las sucursales incluida la central, ya podían trabajar sin que el sistema cayera al hacer un pedido de compras. Además se adquirió dos armarios rack para alojar todos los servidores que ibamos a usar para los siguientes proyectos, una nueva UPS capaz de mantener todo el contenido de los armarios durante 10-15 minutos y se convirtió un _trastero_ en una sala de servidores.

Quien quiera más detalles que me contacte y con un café en mano, podemos hablar de cualquier detalle.

***

Volver a experiencia [aquí](https://amadorsoy.github.io/proyectos/)