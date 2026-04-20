## 🖼️ Diagrama general de la arquitectura del sistema.



**Descripción:**  
La arquitectura general propuesta permite identificar la integración de diferentes módulos entre los que son fácilmente destacables módulos como el del gestor de eventos, el gestor de recursos comunitarios, el sistema de reservas, la geolocalización del espacio y sistema de medición de satisfacción ciudadana.


### 📷 Diagrama
![Figura3](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura3.png)

### 🧾 Código de Figura 3
```plantuml
@startuml

actor Usuario

rectangle "Interfaz (Web / App)" {
  Usuario --> UI
}

rectangle "Sistema de Gestión Comunitaria" {

  rectangle "Módulos principales" {
    [Gestión de Eventos]
    [Sistema de Reservas]
    [Gestión de Recursos]
    [Satisfacción Ciudadana]
  }

  rectangle "Servicios" {
    [Geolocalización]
    [Autenticación y Seguridad]
  }

  rectangle "Datos" {
    [Base de Datos]
  }

}

UI --> [Gestión de Eventos]
UI --> [Sistema de Reservas]

[Gestión de Eventos] --> [Sistema de Reservas]
[Gestión de Eventos] --> [Geolocalización]

[Sistema de Reservas] --> [Gestión de Recursos]

[Gestión de Eventos] --> [Base de Datos]
[Sistema de Reservas] --> [Base de Datos]
[Satisfacción Ciudadana] --> [Base de Datos]

[Gestión de Eventos] --> [Autenticación y Seguridad]
[Sistema de Reservas] --> [Autenticación y Seguridad]

@enduml