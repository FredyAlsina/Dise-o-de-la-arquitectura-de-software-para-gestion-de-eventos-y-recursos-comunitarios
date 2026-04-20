## 🖼️ Marco general de la propuesta arquitectónica del sistema.



**Descripción:**  
Se muestra una vista general de la arquitectura que se propone, en la que se integran los diferentes elementos del sistema y se hace evidente la forma en que se realiza la interacción de estos para ofrecer una solución tecnológica orientada hacia la gestión de eventos y la gestión de los recursos comunitarios.



### 📷 Diagrama
![Figura19](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura19.png)

### 🧾 Código de Figura 19
```plantuml
@startuml

left to right direction
skinparam componentStyle rectangle

' ===== ACTORES =====
actor Ciudadano
actor "Gestor Comunitario" as Gestor
actor Administrador

' ===== PRESENTACIÓN =====
rectangle "Capa de Presentación" {
  [Web / App] as UI
}

' ===== API / BACKEND =====
rectangle "Capa de Aplicación (API)" {
  [API REST] as API
}

' ===== LÓGICA DE NEGOCIO =====
rectangle "Capa de Lógica de Negocio" {

  [Gestión de Eventos] as Eventos
  [Sistema de Reservas] as Reservas
  [Gestión de Recursos] as Recursos
  [Satisfacción Ciudadana] as Satisfaccion
  [Gestión de Usuarios] as Usuarios

}

' ===== SERVICIOS =====
rectangle "Servicios Externos / Integraciones" {

  [Geolocalización] as Geo
  [Difusión y Notificaciones] as Difusion

}

' ===== SEGURIDAD =====
rectangle "Seguridad (Transversal)" {
  [Autenticación y Autorización] as Seguridad
}

' ===== DATOS =====
database "Base de Datos" as DB

' ===== INFRAESTRUCTURA (ESCALABILIDAD) =====
cloud "Infraestructura Cloud / Contenedores" {
  [Servidor de Aplicación]
  [Servidor de Base de Datos]
}

' ===== INTERACCIONES =====

' Actores
Ciudadano --> UI
Gestor --> UI
Administrador --> UI

' Flujo principal
UI --> API

API --> Eventos
API --> Reservas
API --> Usuarios

' Lógica interna
Eventos --> Reservas
Reservas --> Recursos

Eventos --> Satisfaccion

' Servicios externos
Eventos --> Geo
Eventos --> Difusion

' Datos
Eventos --> DB
Reservas --> DB
Recursos --> DB
Usuarios --> DB
Satisfaccion --> DB

' Seguridad transversal
API --> Seguridad
Eventos --> Seguridad
Reservas --> Seguridad
Usuarios --> Seguridad

' Infraestructura
API --> "Servidor de Aplicación"
DB --> "Servidor de Base de Datos"

@enduml