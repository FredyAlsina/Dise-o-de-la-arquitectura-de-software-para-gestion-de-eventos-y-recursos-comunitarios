## 🖼️ Diagrama de casos de uso de actores involucrados en el sistema de gestión Comunitaria.



**Descripción:**  
El diagrama de casos de uso presentado a continuación permite conocer las principales interacciones de los actores del sistema y las funciones que proporciona la plataforma de gestión de eventos, recursos y espacios comunitarios.

El modelo se ha definido con tres actores clave: ciudadano, gestor comunitario y administrador. Cada uno de los actores tiene definido un papel o función dentro del propio sistema, ofreciendo de este modo una clara separación de responsabilidades y un adecuado control del acceso a las funcionalidades.


### 📷 Diagrama
![Figura2](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura2.png)

### 🧾 Código de Figura 2
```plantuml
@startuml

left to right direction

actor Ciudadano
actor Administrador
actor "Gestor Comunitario" as Gestor

rectangle "Sistema de Gestión Comunitaria" {

  (Consultar eventos) as CE
  (Reservar espacio) as RE
  (Ver ubicación de eventos) as GEO
  (Calificar evento) as CAL
  (Iniciar sesión) as LOGIN
  
  (Registrar evento) as REG
  (Gestionar recursos) as GR
  (Administrar usuarios) as AU

}

' Ciudadano
Ciudadano --> CE
Ciudadano --> RE
Ciudadano --> CAL

' Gestor
Gestor --> REG
Gestor --> CE

' Administrador
Administrador --> AU
Administrador --> GR
Administrador --> CE

' Relaciones include (seguridad)
RE --> LOGIN : <<include>>
REG --> LOGIN : <<include>>
CAL --> LOGIN : <<include>>
GR --> LOGIN : <<include>>
AU --> LOGIN : <<include>>

' Relación funcional
CE --> GEO : <<include>>

@enduml