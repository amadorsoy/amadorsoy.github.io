# Virtualización

## Proyecto

En mi andadura por Maderas Santana, S.L. la estructura del departamento de sistemas estaba compuesta por el jefe de departamento y yo mismo, en aquel momento mi jefe de departamento me indica que tenemos que ver una solución de virtualización y me comenta los dos sistemas que tendríamos que analizar: VMWare y [Red Hat KVM](https://www.redhat.com/es/topics/virtualization/what-is-KVM). Cabe indicar que en ese momento las dos soluciones que se analizaban eran completamente gratuitas, la versión de ESXi era gratuita y ofrecía lo mismo que su hermana licenciada, pero con algunas limitaciones como que no permitía la migración entre hosts de maquinas clientes en caliente, pero era muy funcional. Y por su parte KVM sobre CentOS era también completamente gratuita.

A partir de ese momento me pongo a montar sobre un equipo la solución de [VMWare ESXi](https://es.wikipedia.org/wiki/VMware_ESXi) como servidor de virtualización y un cliente virtualizado, comprobar con qué herramientas podíamos contar con VMWare de cara a la instalación, mantenimiento y gestión de las máquinas virtuales. Tras completar la pequeña lista de cosas que tenía que evaluar, formatear e instalar un CentOS para usar KVM, montar la misma estructura y por supuesto analizar los mismos puntos.

En ese momento del análisis la solución de VMWare ofrecía mejores herramientas de administración y gestión. Además el rendimiento con la red era un poco mayor. Finalmente se escogió VMWare ESXi. A partir de ese momento, migración de ordenadores físicos a la solución de virtualización.

Por supuesto, mi jefe de departamento tuvo la visión en ese momento de iniciar el proceso de virtualización y aprovechar la arquitectura que teníamos para sacarle mejor rendimiento con la ampliación de memoria correspondiente.

De esta forma tan práctica tuve mi acercamiento a VMWare, después de eso vendrían unos cuantos años de administración de los servidores virtualizados y una estrecha relación con VMWare.