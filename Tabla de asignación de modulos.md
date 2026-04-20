### ASIGNACIÓN DE MÓDULOS POR CAPA


  #### Distribución de los módulos funcionales del sistema en cada capa de la arquitectura, mostrando la separación de responsabilidades.


| Capa                | Módulos asociados                                          |
| :------------------ | :--------------------------------------------------------- |
| `Presentación`      | Interfaz Web / App                                         |
| `Aplicación`        | API REST                                                   |
| `Lógica de negocio` | Gestión de Eventos, Gestión de Reservas, Gestión de Recursos, Satisfacción Ciudadana |
| `Servicios`         | Geolocalización, Difusión de eventos                       |
| `Seguridad`         | Autenticación JWT, Control de acceso por roles (RBAC)      |
| `Datos`             | Base de datos, Repositorio de usuarios, Repositorio de eventos, Repositorio de reservas |