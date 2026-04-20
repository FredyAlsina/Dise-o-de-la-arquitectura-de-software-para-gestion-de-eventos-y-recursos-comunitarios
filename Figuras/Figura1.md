## 🖼️ Sistema de Gestión de Eventos y Recursos Comunitarios

**Descripción:**  
La ilustración muestra de manera general el contexto del sistema de gestión comunitaria, en el cual se identifican los actores primordiales (ciudadano, gestor comunitario y administrador) y su interacción con la plataforma. Así mismo, se muestran las funcionalidades básicas de cada uno de los actores, como el modo de la interacción y la integración del sistema a un servicio externo de geolocalización para consultar las ubicaciones de los eventos y potenciar la funcionalidad del sistema.

### 📷 Diagrama
![Figura1](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/9417de2393776505adb85f43198ee17b33e4b8ed/ImagenesFiguras/Figura1.png)

### 🧾 Código de Figura 1
```plantuml
@startuml

actor Ciudadano
actor "Gestor Comunitario" as Gestor
actor Administrador

rectangle "Sistema de Gestión Comunitaria" as Sistema

' Interacciones
Ciudadano --> Sistema : Consulta eventos\nReserva espacios\nCalifica eventos
Gestor --> Sistema : Crea y gestiona eventos
Administrador --> Sistema : Administra usuarios\nGestiona recursos

' Servicios externos
cloud "Servicio de Geolocalización" as Geo

Sistema --> Geo : Consulta ubicación

@enduml