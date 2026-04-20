### MATRIZ DE TRAZABILIDAD ARQUITECTÓNICA


  #### Correspondencia entre los requerimientos funcionales del sistema y los componentes de la arquitectura que los soportan.

  La matriz de trazabilidad mostrada permite evidenciar la correspondencia entre los requerimientos funcionales que el sistema debe manejar y con los componentes descritos en la arquitectura, de manera que cada funcionalidad que se haya podido identificar en la fase de análisis, esté adecuadamente soportada en el diseño. Se logra así que la propuesta arquitectónica sea coherente, verificable y completa.


| ID        | Requerimiento             | Componente                    | Capa                  |
| :-------- | :------------------------ | :---------------------------- | :-------------------- |
| `RF01`  | `Consultar eventos`         | Módulo de eventos             | Lógica de negocio     |
| `RF02`  | `Ver ubicación de eventos`  | Servicio de geolocalización   | Servicios             |
| `RF03`  | `Registrar usuario`         | Módulo de usuarios            | Lógica de negocio     |
| `RF04`  | `Iniciar sesión`            | Módulo de autenticación       | Seguridad             |
| `RF05`  | `Reservar espacio`          | Sistema de reservas           | Lógica de negocio     |
| `RF06`  | `Crear evento`              | Módulo de eventos             | Lógica de negocio     |
| `RF07`  | `Gestionar eventos`         | Módulo de eventos             | Lógica de negocio     |
| `RF08`  | `Administrar usuarios`      | Gestión de usuarios           | Lógica de negocio     |
| `RF09`  | `Gestionar recursos`        | Gestión de recursos           | Lógica de negocio     |
| `RF10`  | `Calificar eventos`         | Módulo de satisfacción        | Lógica de negocio     |