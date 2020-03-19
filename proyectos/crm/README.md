# Al rico CRM: datos y más datos.

Volver a experiencia [aquí](https://amadorsoy.github.io/proyectos/)

***

La estrategia en ventas es fundamental, pero no puedes desarrollar ninguna sin basarte en los datos. Era necesario aportar al departamento de Ventas y Marketing una herramienta con la que sacar los datos que necesitaban para tomar decisiones rápidas, preparar campañas, etc.

Tal y como ya he comentado en [Flotas](https://amadorsoy.github.io/proyectos/gestionflotas/), me encargo de la base de datos y del API, en este caso no se requería crear una estructura más o menos compleja de datos, sino de crear un sistema de consultas que pudieran generarse dinámicamente en base a las peticiones de los usuarios y que devolviera los datos requeridos en un tiempo prudencialmente rápido.

De nuevo aparecía Python y [Flask](https://flask.palletsprojects.com/en/1.1.x/), para crear el proyecto CRM. Y tras saber de forma concreta lo qué solicitaba el departamento, sin que para ello hubiera que mandar un satelite a la cara oculta de la Luna, empece con los procedimientos en la base de datos que me deberían dar entre otros: [paretos](https://es.wikipedia.org/wiki/Diagrama_de_Pareto), resúmenes de consumos y comparativos entre períodos de tiempo. Vamos lo normal en estos casos.

Posteriormente se han ido añadiendo más funcionalidades al CRM, por lo que se ha tenido que agregar permisología. Pero seguimos teniendo una estructura que se puede virtualizar o dockerizar y por lo tanto es más o menos escalable sin muchos gastos.

***

Volver a experiencia [aquí](https://amadorsoy.github.io/proyectos/)