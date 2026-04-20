## 🖼️ Vista de despliegue conceptual de la arquitectura propuesta.



**Descripción:**  
La vista de despliegue describe la distribución física de los componentes del sistema en la infraestructura tecnológica, identificando los nodos principales y las conexiones entre ellos.



### 📷 Diagrama
![Figura16](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura16.png)

### 🧾 Código de Figura 16
```plantuml
@startuml

node "Cliente (Web / App)" {
  component "Interfaz de Usuario"
}

node "Servidor de Aplicación" {
  component "API REST"
  component "Módulo de Eventos"
  component "Módulo de Reservas"
  component "Módulo de Recursos"
  component "Módulo de Satisfacción"
  component "Seguridad"
}

node "Servidor de Base de Datos" {
  database "Base de Datos"
}

cloud "Servicios Externos" {
  component "Geolocalización"
  component "Difusión / Notificaciones"
}

' Conexiones
"Interfaz de Usuario" --> "API REST"
"API REST" --> "Módulo de Eventos"
"API REST" --> "Módulo de Reservas"

"Módulo de Eventos" --> "Base de Datos"
"Módulo de Reservas" --> "Base de Datos"
"Módulo de Recursos" --> "Base de Datos"
"Módulo de Satisfacción" --> "Base de Datos"

"Módulo de Eventos" --> "Geolocalización"
"Módulo de Eventos" --> "Difusión / Notificaciones"

@enduml