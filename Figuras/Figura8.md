## 🖼️ Seguridad transversal en la arquitectura del sistema



**Descripción:**  
La figura representa la integración de mecanismos de seguridad en todas las capas del sistema.



### 📷 Diagrama
![Figura8](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura8.png)

### 🧾 Código de Figura 8
```plantuml
@startuml
package "Capa de Presentación" {
  [Interfaz de Usuario]
}

package "Capa de Aplicación" {
  [API REST]
}

package "Capa de Negocio" {
  [Lógica de negocio]
}

package "Capa de Datos" {
  [Base de datos]
}

[Interfaz de Usuario] --> [API REST]
[API REST] --> [Lógica de negocio]
[Lógica de negocio] --> [Base de datos]

rectangle "Seguridad (Transversal)" {
  [Autenticación]
  [Autorización]
  [Validación]
}

[Autenticación] ..> [API REST]
[Autorización] ..> [Lógica de negocio]
[Validación] ..> [Base de datos]
@enduml