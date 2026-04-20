## 🖼️ Arquitectura de software basada en capas.



**Descripción:**  
En la figura se presenta la arquitectura del sistema de gestión de eventos y recursos comunitarios estructurado en capas, como por ejemplo la capa de presentación, capa de aplicación, capa de lógica de negocio, capa de servicios y capa de datos. Cada capa del sistema de gestión de eventos y recursos comunitarios tiene una función concreta que facilita la modularidad, escalabilidad y mantenimiento del mismo, además de incorporar un sistema transversal de seguridad para la autenticación y autorización de los usuarios.


### 📷 Diagrama
![Figura4](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura4.png)

### 🧾 Código de Figura 4
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
  [Gestión de Reservas]
  [Satisfacción Ciudadana]
}

package "Capa de Servicios" {
  [Geolocalización]
  [Difusión de Eventos]
}

package "Seguridad (Transversal)" {
  [Autenticación y Autorización]
}

package "Capa de Datos" {
  [Base de Datos]
}

[Interfaz Web / App] --> [API REST]
[API REST] --> [Gestión de Eventos]
[API REST] --> [Gestión de Reservas]

[Gestión de Eventos] --> [Geolocalización]
[Gestión de Eventos] --> [Difusión de Eventos]

[Gestión de Eventos] --> [Base de Datos]
[Gestión de Reservas] --> [Base de Datos]
[Satisfacción Ciudadana] --> [Base de Datos]

@enduml