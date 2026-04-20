## 🖼️ Flujo general del proceso de gestión de eventos comunitarios.



**Descripción:**  
Para conseguir una comprensión del funcionamiento del sistema, los principales procesos productivos se dan a conocer a través de los diagramas de flujos, que ilustran explícitamente y de manera secuencial las actividades, decisiones y actores participantes de cada proceso. 



### 📷 Diagrama
![Figura12](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura12.png)

### 🧾 Código de Figura 12
```plantuml
@startuml

start

:Iniciar sesión (Gestor);

:Crear evento;

:Ingresar datos del evento;

if (¿Datos válidos?) then (Sí)
  :Guardar evento;
  :Publicar evento;
else (No)
  :Corregir información;
endif

:Ciudadano consulta evento;

stop

@enduml