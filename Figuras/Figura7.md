## 🖼️ Esquema de protección de datos del sistema



**Descripción:**  
La figura ilustra los mecanismos de protección de la información mediante conexiones seguras y almacenamiento cifrado.



### 📷 Diagrama
![Figura7](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura7.png)

### 🧾 Código de Figura 7
```plantuml
@startuml
actor Usuario
participant "Cliente Web/App" as Client
participant "Servidor (API)" as Server
database "Base de Datos" as DB

Usuario -> Client : Solicitud
Client -> Server : HTTPS (Datos seguros)
Server -> DB : Consulta / Guardado

note right of Server
Datos protegidos
Validación de entrada
end note

note right of DB
Contraseñas cifradas
Datos protegidos
end note
@enduml