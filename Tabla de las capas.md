### ARQUITECTURA EN CAPAS DEL SISTEMA


  #### Descripción de las capas que conforman la arquitectura del sistema, sus funciones y los componentes principales asociados a cada una.

  La tabla presenta las capas que forman la base de la arquitectura del sistema de gestión de eventos y recursos del contexto, las cuales se encuentran especificadas con su función y los principales componentes correspondientes. Esta estructura por capas permite al propio sistema tener la separación de responsabilidades, de manera que también se podría decir que aumenta, ya que mejora la mantenibilidad, mantenibilidad, escalabilidad y seguridad del sistema.


| Capa                    | Descripción                                                                                          | Componentes principales                        |
| :---------------------- | :--------------------------------------------------------------------------------------------------- | :--------------------------------------------- |
| `Presentación`          | Permite la interacción entre los usuarios y el sistema a través de interfaces web o móviles          | Interfaz Web / App                             |
| `Aplicación`            | Actúa como intermediaria mediante una API REST, gestionando las solicitudes del usuario              | API REST                                       |
| `Lógica de Negocio`     | Contiene los módulos que gestionan los procesos principales del sistema                              | Gestión de eventos, reservas, satisfacción     |
| `Servicios`             | Proporciona funcionalidades externas o especializadas que apoyan la lógica del sistema               | Geolocalización, difusión de eventos           |
| `Seguridad`             | Gestiona la autenticación y autorización de los usuarios de forma transversal en todas las capas     | Autenticación JWT, control de acceso RBAC      |
| `Datos`                 | Se encarga de la persistencia, almacenamiento y recuperación de la información del sistema           | Base de datos, repositorios de información     |