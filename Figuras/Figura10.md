## 🖼️ Diagrama de componentes



**Descripción:**  
El diagrama de componentes muestra la estructura interna del sistema de gestión comunitaria, y muestra la disposición y relaciones que mantienen los módulos más importantes.



### 📷 Diagrama
![Figura10](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura10.png)

### 🧾 Código de Figura 10
```plantuml
@startuml

package "Sistema de Gestión Comunitaria" {

  [Frontend Web/App] as Frontend
  [API Backend] as API

  package "Módulos de Negocio" {
    [Gestión de Eventos] as Eventos
    [Gestión de Reservas] as Reservas
    [Gestión de Satisfacción] as Satisfaccion
  }

  package "Servicios" {
    [Servicio de Geolocalización] as Geo
    [Servicio de Difusión] as Difusion
    [Servicio de Seguridad] as Seguridad
  }

  package "Persistencia" {
    [Base de Datos] as BD
  }
}

' Flujo principal
Frontend --> API

API --> Eventos
API --> Reservas
API --> Satisfaccion

' Conexión con servicios
Eventos --> Geo
Eventos --> Difusion

Reservas --> Geo

API --> Seguridad

' Persistencia
Eventos --> BD
Reservas --> BD
Satisfaccion --> BD

@enduml