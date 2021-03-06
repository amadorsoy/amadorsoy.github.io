# Virtualización -  Desde la Era del Hiero a la Nube

Volver a experiencia [aquí](https://amadorsoy.github.io/proyectos/)

***

Corrían tiempos complicados, donde el _Hierro_ empezaba a ser un problema para las estructuras empresariales, en aquella época aparecieron varias _fuerzas blancas_ que intentaban ayudar a sobrevivir al fin de los tiempos del hierro y perdurar en los siguientes años.

Dada mi condición de mago me tocó investigar dos de estas fuerzas **VMWare** y **KVM de Red Hat**. Apliqué las mismas normas y el mismo protócolo para analizar estos _sistemas_. La lista de habilidades y pócimas usadas para las pruebas fueron:

- Host: un equipo con no mucha memoría ya que escaseaban por aquellos tiempos los recursos y así se veía el rendimiento con bajos recursos.
- Fuerzas:
  - VMWare ESXI: la versión [VMWare ESXi](https://es.wikipedia.org/wiki/VMware_ESXi) en aquel momento era gratuita y muy funcional.
  - KVM Red Hat: [Red Hat KVM](https://www.redhat.com/es/topics/virtualization/what-is-KVM) en ese momento instalada sobre CentOS.
- Protocotolo (receta):
  - Eliminar todos los datos del Host, proceso conocido por _formateo_.
  - Instalar una de las fuerzas, primero **KVM** y luego mismo proceso para instalar **VMWARE**.
  - Configurar el Host para poder realizar tareas de instalación, configuración y administración de sistemas virtualizados.
  - Una vez instalado todo el cliente evaluación de las herramientas de control, supervisión y gestión de las maquinas virtualizadas.
  - Medir rendimiento con bajos recursos, reacción de los sistemas a un pico de trabajo, distribución de los recursos, etc.

Dato nuestro contexto, la fuerza que tendríamos que seguir era **VMWare ESXI** ya que en ese momento facilitaba al departamento las tareas diarias de gestión de maquinas virtuales, así como la migración de servicios existentes a virtualización. Tenía mejor reacción hacía los picos de trabajo y una distribución más eficiente de los recursos.

Desde ese momento hasta la fecha, como _mago con dotes para sistemas_ he podido usar **VMWare** tanto con la licencia gratuita ofrecida con **ESXI** como la licencia profesional, también [_XEN Server_](https://xenserver.org/) y [_OVirt_](https://www.ovirt.org/).

Hoy día tenemos Docker, Kubernetes y otros sistemas para poder _"servir"_ servicios, pero la virtualización fue un paso para aliviar el gasto en muchos departamentos y empresas.


***
Volver a experiencia [aquí](https://amadorsoy.github.io/proyectos/)