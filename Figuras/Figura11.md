## 🖼️ Relación entre capas y módulos funcionales.



**Descripción:**  
La figura muestra la relación existente entre las capas de la arquitectura y los módulos funcionales del sistema de gestión de eventos y de recursos comunitarios, de tal forma que cada módulo funcional queda representado en su respectivo lugar en la estructura por capas. Esta representación permite comprender el flujo de información entre los componentes, así como las dependencias entre los mismos, facilitando así el diseño, la integración y la evolución del sistema.



### 📷 Diagrama
![Figura11](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura11.png)

### 🧾 Código de Figura 11
```plantuml
@startuml

top to bottom direction

package "Capa de Presentación" {
  [Interfaz Web / App]
}

package "Capa de Aplicación" {
  [API REST]
}

package "Capa de Lógica de Negocio" {
  [Gestión de Eventos]
  [Sistema de Reservas]
  [Gestión de Recursos]
  [Satisfacción Ciudadana]
}

package "Capa de Servicios" {
  [Geolocalización]
  [Difusión de Eventos]
}

package "Capa de Datos" {
  [Base de Datos]
}

package "Seguridad (Transversal)" {
  [Autenticación y Autorización]
}

' Flujo
[Interfaz Web / App] --> [API REST]

[API REST] --> [Gestión de Eventos]
[API REST] --> [Sistema de Reservas]

[Gestión de Eventos] --> [Geolocalización]
[Gestión de Eventos] --> [Difusión de Eventos]

[Sistema de Reservas] --> [Gestión de Recursos]

[Gestión de Eventos] --> [Base de Datos]
[Sistema de Reservas] --> [Base de Datos]
[Satisfacción Ciudadana] --> [Base de Datos]

' Seguridad transversal
[Gestión de Eventos] --> [Autenticación y Autorización]
[Sistema de Reservas] --> [Autenticación y Autorización]

@enduml