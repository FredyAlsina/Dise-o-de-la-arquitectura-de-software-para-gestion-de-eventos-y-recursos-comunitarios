## 🖼️ Modelo de autorización basado en roles



**Descripción:**  
Ciudadano, Gestor comunitario, Administrador. Cada rol posee permisos concretos que restringen el acceso a funcionalidades claves del sistema.
La aplicación de un modelo de autorización basado en roles implementa una estructura clara de permisos dentro del sistema que evita accesos no deseados a funcionalidades delicadas. Este sistema simplifica la gestión del sistema ya que facilita la posibilidad de dar permisos, cambiarlos o deshabilitarlos mediante un mecanismo centralizado acorde a las necesidades del funcionamiento, garantizando de esta forma que cada usuario pueda acceder solamente a las funcionalidades que se espera que tenga acceso, reduciendo los riesgos y aumentando la seguridad y control del sistema interno.



### 📷 Diagrama
![Figura6](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura6.png)

### 🧾 Código de Figura 6
```plantuml
@startuml
actor Ciudadano
actor "Gestor Comunitario" as Gestor
actor Administrador

rectangle "Sistema" {
    usecase "Consultar eventos" as UC1
    usecase "Reservar espacio" as UC2
    usecase "Crear evento" as UC3
    usecase "Administrar usuarios" as UC4
}

Ciudadano --> UC1
Ciudadano --> UC2

Gestor --> UC3

Administrador --> UC4
@enduml