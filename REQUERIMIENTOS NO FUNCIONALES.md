### TABLA DE REQUERIMIENTOS NO FUNCIONALES


  #### Definición de los atributos de calidad que determinan cómo debe comportarse el sistema más allá de sus funcionalidades.


| ID        | Tipo     | Descripción                 |
| :-------- | :------- | :-------------------------- |
| `RNF01` | `Seguridad` | Autenticación mediante JWT y autorización por roles (RBAC) para proteger el acceso a las funcionalidades del sistema |
| `RNF02` | `Escalabilidad` | El sistema debe soportar múltiples usuarios concurrentes sin degradar su rendimiento |
| `RNF03` | `Disponibilidad` | El sistema debe garantizar acceso continuo y operación estable ante posibles fallos |
| `RNF04` | `Usabilidad` | La interfaz debe ser intuitiva y accesible desde dispositivos web y móviles para distintos perfiles de usuario |
| `RNF05` | `Mantenibilidad` | El código debe ser modular para facilitar modificaciones, correcciones y evolución del sistema |
| `RNF06` | `Interoperabilidad` | El sistema debe integrarse con APIs externas, especialmente el servicio de geolocalización |
| `RNF07` | `Rendimiento` | El tiempo de respuesta ante solicitudes del usuario no debe superar los 2 segundos |