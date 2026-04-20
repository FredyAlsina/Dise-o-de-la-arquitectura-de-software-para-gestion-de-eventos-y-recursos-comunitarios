## 🖼️ Vista lógica de la arquitectura del sistema.



**Descripción:**  
A continuación, se da forma a la vista lógica de la arquitectura, que describe la organización interna de los componentes del sistema y la forma en que se relacionan entre sí para cumplir los requerimientos funcionales.

Con esta vista se puede determinar los diferentes módulos del sistema e interpretar cómo interactúan junto a los elementos de la capa de negocio para procesar eventos, reservas, recursos y usuarios.




### 📷 Diagrama
![Figura9](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura9.png)

### 🧾 Código de Figura 9
```plantuml
@startuml

package "Vista Lógica - Sistema de Gestión Comunitaria" {

  [Gestión de Eventos] as Eventos
  [Sistema de Reservas] as Reservas
  [Gestión de Recursos] as Recursos
  [Gestión de Usuarios] as Usuarios
  [Satisfacción Ciudadana] as Satisfaccion
  [Seguridad (Autenticación y Autorización)] as Seguridad

  database "Base de Datos" as BD
}

' Relaciones principales
Eventos --> Reservas : Coordina reservas
Reservas --> Recursos : Consulta disponibilidad

Eventos --> Satisfaccion : Genera evaluación
Usuarios --> Seguridad : Validación de acceso

Eventos --> BD
Reservas --> BD
Recursos --> BD
Usuarios --> BD
Satisfaccion --> BD

' Seguridad transversal
Eventos --> Seguridad
Reservas --> Seguridad
Usuarios --> Seguridad

@enduml