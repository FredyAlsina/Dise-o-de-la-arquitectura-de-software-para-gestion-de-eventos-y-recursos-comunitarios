### COMPONENTES DE DESPLIEGUE DEL SISTEMA


  #### Distribución de los componentes del sistema según los entornos de infraestructura y las funciones que cumplen en cada uno.

  La tabla muestra los componentes de despliegue del sistema según se distribuyen por los entornos y las funciones que cumplen en cada uno de ellos. Esta distribución facilita el entendimiento de los componentes del sistema en la infraestructura del mismo, la manera en la que se da la interacción entre cliente, servidor y con los servicios externos, además de asegurar el correcto funcionamiento de la plataforma.


| Entorno                   | Componentes desplegados                              | Función                                          |
| :------------------------ | :--------------------------------------------------- | :----------------------------------------------- |
| `Cliente (Web / App)`     | Interfaz de usuario                                  | Permite la interacción del usuario con el sistema |
| `Servidor de aplicación`  | API REST, módulos del sistema, seguridad JWT/RBAC    | Procesa la lógica del sistema y gestiona solicitudes |
| `Servidor de base de datos` | Base de datos                                      | Almacena y recupera la información del sistema   |
| `Servicios externos`      | Geolocalización, notificaciones                      | Proveen funcionalidades especializadas de apoyo  |