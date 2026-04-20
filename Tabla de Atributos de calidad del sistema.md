### ATRIBUTOS DE CALIDAD DEL SISTEMA


  #### Definición de los atributos de calidad que guían las decisiones arquitectónicas del sistema y la forma en que cada uno se implementa.

  En la tabla se encuentran los atributos principales de calidad del sistema, así como la descripción de cada uno de ellos y, en el último campo de la tabla, la identificación de los mecanismos habilitados para garantizar su cumplimiento. De esta manera, se logrará un sistema robusto, seguro y adaptable en base a buenas prácticas de diseño de arquitectura de software.


| Atributo              | Descripción                                                                          | Cómo se implementa                              |
| :-------------------- | :----------------------------------------------------------------------------------- | :---------------------------------------------- |
| `Seguridad`           | Protege la información y controla el acceso al sistema                               | Autenticación JWT y autorización por roles RBAC |
| `Escalabilidad`       | Permite que el sistema crezca sin afectar su rendimiento                             | Arquitectura modular con capas independientes   |
| `Disponibilidad`      | Garantiza que el sistema esté accesible cuando se requiera                           | Infraestructura distribuida y degradación controlada |
| `Mantenibilidad`      | Facilita la modificación, corrección y actualización del sistema                     | Separación por capas y diseño modular           |
| `Interoperabilidad`   | Permite la integración con otros sistemas y servicios externos                       | API REST con formato JSON                       |