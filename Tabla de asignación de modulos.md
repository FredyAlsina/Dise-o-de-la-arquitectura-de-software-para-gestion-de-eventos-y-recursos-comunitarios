### ASIGNACIÓN DE MÓDULOS POR CAPA


  #### Distribución de los módulos funcionales del sistema en cada capa de la arquitectura, mostrando la separación de responsabilidades.

  La tabla presenta la distribución de los módulos del sistema de gestión que organiza los eventos y recursos comunitarios a partir de las capas que conforman la arquitectura, lo que da cuenta de cómo se distribuyen las funcionalidades centrales en el sistema a partir de una suficiente separación de responsabilidades y de una estructura coherente del propio sistema.


| Capa                | Módulos asociados                                          |
| :------------------ | :--------------------------------------------------------- |
| `Presentación`      | Interfaz Web / App                                         |
| `Aplicación`        | API REST                                                   |
| `Lógica de negocio` | Gestión de Eventos, Gestión de Reservas, Gestión de Recursos, Satisfacción Ciudadana |
| `Servicios`         | Geolocalización, Difusión de eventos                       |
| `Seguridad`         | Autenticación JWT, Control de acceso por roles (RBAC)      |
| `Datos`             | Base de datos, Repositorio de usuarios, Repositorio de eventos, Repositorio de reservas |