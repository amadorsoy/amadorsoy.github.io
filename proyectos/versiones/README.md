# Desplegando las naves

Volver a experiencia [aquí](https://amadorsoy.github.io/proyectos/)

***

Cuando trabajas en una empresa que no produce software, tus usuarios son tus propios compañeros de trabajo y las distintas tiendas que tiene la empresa son las ubicaciones donde están los ordenadores que hay que actualizar cuando hay un cambio de versión en el software.

No había nada en la empresa, por lo que había que pensar un sistema de actualización que se encargará de controlar en qué versión esta un programa y si cambia, tendría que sustituir la aplicación por la nueva versión.

Cuando haces un proyecto, tienes que intentar pensar en tu infraestructura actual, dejando abierta la posibilidad al cambio, porque quien sabe cómo estará la empresa mañana. Con las herramientas y dispositivos que tenía cree un sistema de actualización de software muy fácil de entender para los compañeros.

Cree un API que lee de una base de datos, aunque se podría cambiar para leer de un fichero json, xml o como se necesite, las versiones de los programas (o archivos porque vale para todo tipo de archivos) y cuando le haces una consulta te indica la versión y el lugar de donde descargarse la actualización en caso de ser necesario.

Luego cree un programa que se encargaba de leer un archivo de configuración todo lo que tiene que comprobar que hay que actualizar y según el archivo consulta al API. Compara la respuesta del API con lo que el programa tiene y si es necesario actualiza la versión del software y los datos de los archivos que ha cambiado en su configuración. Finalmente el programa tras actualizar, ejecuta el la aplicación que corresponda.

De esta forma tan simple tenemos el software siempre actualizado. Cuando hay necesidad, es decir urgencia, a través de un sistema de notificaciones interno se comunica a los usuarios que cierren la aplicación y vuelvan a abrirla. En ese momento no están ejecutando la aplicación realmente, sino el programa que actualiza, se hace el cambio de versión y se abre la nueva versión. Cuando no hay prisa, como siempre se apagan los ordenadores, al siguiente día se actualizarán todos.

Los usuarios no tienen nada más que hacer y tenemos todo el software actualizado.


***

Volver a experiencia [aquí](https://amadorsoy.github.io/proyectos/)