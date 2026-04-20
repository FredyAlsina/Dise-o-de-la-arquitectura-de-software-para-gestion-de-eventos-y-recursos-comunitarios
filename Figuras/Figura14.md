## 🖼️ Vista conceptual de la gestión de usuarios y roles del sistema.



**Descripción:**  
El diagrama de clases muestra la estructura estática del sistema, permitiendo identificar las entidades fundamentales, sus atributos, métodos y relaciones.



### 📷 Diagrama
![Figura14](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura14.png)

### 🧾 Código de Figura 14
```plantuml
@startuml

class Usuario {
  id: int
  nombre: string
  correo: string
  rol: string
  +iniciarSesion()
}

class Evento {
  id: int
  nombre: string
  fecha: Date
  ubicacion: string
  estado: string
  +crearEvento()
  +editarEvento()
  +publicarEvento()
}

class Reserva {
  id: int
  fecha: Date
  estado: string
  +crearReserva()
  +cancelarReserva()
}

class Recurso {
  id: int
  nombre: string
  cantidad: int
  +asignarRecurso()
}

class Espacio {
  id: int
  nombre: string
  capacidad: int
}

class Encuesta {
  id: int
  calificacion: int
  comentario: string
  +registrarCalificacion()
}

' Relaciones
Usuario "1" --> "0..*" Evento : crea
Usuario "1" --> "0..*" Reserva : realiza

Evento "1" --> "0..*" Reserva
Evento "1" --> "0..*" Recurso
Evento "1" --> "0..*" Encuesta

Reserva "1" --> "1" Espacio

@enduml