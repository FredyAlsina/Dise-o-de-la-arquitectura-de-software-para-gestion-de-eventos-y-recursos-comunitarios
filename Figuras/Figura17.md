## 🖼️ Diagrama en bloques más atributos de calidad



**Descripción:**  
El diagrama en bloques muestra la arquitectura general del sistema y su asociación con las definiciones de calidad, que muestran como la organización de los componentes contribuye a la satisfacción de los aspectos de calidad que se pretenden: Interoperabilidad, seguridad, escalabilidad, disponibilidad y mantenibilidad. También permite una visión amplia de la configuración del sistema y el alineamiento con los objetivos de calidad definidos.



### 📷 Diagrama
![Figura17](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura17.png)

### 🧾 Código de Figura 17
```plantuml
@startuml

skinparam componentStyle rectangle

package "Arquitectura del Sistema" {

  [Capa de Presentación] as UI
  [Capa de Aplicación] as API
  [Lógica de Negocio] as LN
  [Capa de Datos] as BD

}

package "Atributos de Calidad" {

  cloud "Seguridad" as Seg
  cloud "Escalabilidad" as Esc
  cloud "Disponibilidad" as Disp
  cloud "Mantenibilidad" as Mant
  cloud "Interoperabilidad" as Inter

}

' Flujo principal
UI --> API
API --> LN
LN --> BD

' Relación atributos con capas
Seg --> API
Seg --> LN

Esc --> API
Esc --> LN

Disp --> API
Disp --> BD

Mant --> LN

Inter --> API

@enduml