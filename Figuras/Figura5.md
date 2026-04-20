## 🖼️ Flujo de autenticación del sistema



**Descripción:**  
La figura representa el proceso de autenticación de usuarios, donde el sistema valida las credenciales ingresadas y genera un token de acceso que permite el uso seguro de las funcionalidades.


### 📷 Diagrama
![Figura5](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura5.png)

### 🧾 Código de Figura 5
```plantuml
@startuml
actor Usuario
participant "Interfaz (Login)" as UI
participant "API REST" as API
participant "Servicio de Autenticación" as Auth
database "Base de Datos" as DB

Usuario -> UI : Ingresa credenciales
UI -> API : Enviar datos login
API -> Auth : Validar credenciales
Auth -> DB : Consultar usuario
DB --> Auth : Datos usuario

alt Credenciales válidas
    Auth --> API : Token JWT
    API --> UI : Acceso permitido
else Credenciales inválidas
    Auth --> API : Error
    API --> UI : Acceso denegado
end
@enduml