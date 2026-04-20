## 🖼️ Diagrama de secuencias y escenario principal de uso.



**Descripción:**  
Se representa la secuencia de interacción de los elementos del sistema durante el proceso de creación de un evento, incluyendo la validación de datos y de autenticación, así como la comunicación entre la API, la capa de presentación, los servicios de negocio y la base de datos para garantizar la correcta ejecución del flujo.



### 📷 Diagrama
![Figura18](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura18.png)

### 🧾 Código de Figura 18
```plantuml
@startuml

actor "Líder Comunitario" as Lider

participant "Frontend (Web/App)" as UI
participant "API REST" as API
participant "Servicio de Eventos" as Eventos
database "Base de Datos" as DB

Lider -> UI : Solicita crear evento
activate UI

UI -> API : Enviar datos del evento
activate API

API -> API : Validar datos / Autenticación

API -> Eventos : Crear evento
activate Eventos

Eventos -> DB : Guardar evento
activate DB

DB --> Eventos : Confirmación
deactivate DB

Eventos --> API : Evento creado
deactivate Eventos

API --> UI : Respuesta exitosa
deactivate API

UI --> Lider : Notificación de éxito
deactivate UI

@enduml