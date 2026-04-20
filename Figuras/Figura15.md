## 🖼️ Diagrama de comunicación entre módulos del sistema.



**Descripción:**  
Se determinó el mecanismo de comunicación entre los diferentes módulos que en conforman la arquitectura del sistema. Esta interacción se encarga de coordinar las operaciones necesarias para la realización del sistema, de modo que se pueda garantizar una correcta transmisión de información entre dichos elementos.



### 📷 Diagrama
![Figura15](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura15.png)

### 🧾 Código de Figura 15
```plantuml
@startuml

component "Interfaz Web/App" as UI
component "API REST" as API
component "Gestión de Eventos" as Eventos
component "Sistema de Reservas" as Reservas
component "Gestión de Recursos" as Recursos
component "Satisfacción Ciudadana" as Satisfaccion
component "Seguridad" as Seguridad
database "Base de Datos" as BD

' Flujo de comunicación
UI --> API : Solicitudes HTTP
API --> Eventos
API --> Reservas

Eventos --> Reservas
Reservas --> Recursos

Eventos --> Satisfaccion

Eventos --> BD
Reservas --> BD
Recursos --> BD
Satisfaccion --> BD

' Seguridad transversal
API --> Seguridad
Eventos --> Seguridad
Reservas --> Seguridad

@enduml