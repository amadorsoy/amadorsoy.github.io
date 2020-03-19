# Al abordaje: gestión de flotas

Volver a experiencia [aquí](https://amadorsoy.github.io/proyectos/)

***

Tocaba empezar a desarrollar algunas nuevas habilidades ya de _mago blanco_ y la primera por la que había que empezar era con un sistema de gestión de flotas que tuviera un panel de administración web y una aplicación para dispositivos móviles que tuvieran los conductores para actualizar repostajes y otros datos.

Como en la empresa solo somos dos los que desarrollamos y nos encargamos de sistemas y bases de datos, yo me encargaría del análisis, desarrollo de la base de datos y del API, mi compañero se encargaría del Front-End y de sistemas. Para este proyecto además, me encargué de realizar la aplicación para dispositivos móviles que interactuaba con el API.

De esta forma podemos seguir trabajando cada uno en nuestras tareas diarias sin depender 100% del trabajo de la otra persona. En ese momento, docker aún no era tan conocido, pero estabamos creando un sistema que podíamos escalar con maquinas virtuales o con docker y [NGinx](https://www.nginx.com/). La planificación y diseño de la sala de servidores ya empezaba a tener su razón de ser.

Para el API de la gestión de flotas use Python y [Flask](https://flask.palletsprojects.com/en/1.1.x/). Con un framework tan modular como Flask, no corríamos el riesgo de sobredimensionar ni el proyecto ni los recursos de máquina y por otro lado nos aportaba lo suficiente para saber que no tendríamos que reinventar la rueda. Usando los entornos aislados con [virtualenv](https://wiki.archlinux.org/index.php/Python_(Espa%C3%B1ol)/Virtual_environment_(Espa%C3%B1ol)), podía desarrollar, subir al repositorio y estar tranquilo porque mi compañero podría descargar el mismo código y con pocos comandos poner a correr mi código.

Para la aplicación móvil, opté por [Ionic](https://ionicframework.com/) con Angular, consumiendo el API, solo tenía que tener una pequeña base de datos en el dispositivo para guardar pocos datos que ayudaran en el consumo de nuestros servicios.


***

Volver a experiencia [aquí](https://amadorsoy.github.io/proyectos/)