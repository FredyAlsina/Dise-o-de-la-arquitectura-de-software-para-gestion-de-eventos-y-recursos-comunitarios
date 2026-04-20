## 🖼️ Flujo general del proceso de gestión de eventos comunitarios.



**Descripción:**  
El sistema lleva a cabo la verificación de la disponibilidad del recurso y las reglas de validación que lo conforma, es decir, las restricciones de uso y conflictos horarios. En el caso de cumplir con las condiciones, se aprueba la reserva y se registra a nivel de sistema, con la respectiva confirmación por parte del usuario. En caso contrario, se notificará el rechazo o la necesidad de ajustar la reserva.



### 📷 Diagrama
![Figura13](https://github.com/FredyAlsina/Dise-o-de-la-arquitectura-de-software-para-gestion-de-eventos-y-recursos-comunitarios/blob/f7f3c44e67a7e5b30375e2d15d6c3acaa55e0152/ImagenesFiguras/Figura13.png)

### 🧾 Código de Figura 13
```plantuml
@startuml

start

:Iniciar sesión (Ciudadano);

:Seleccionar evento o recurso;

:Solicitar reserva;

if (¿Recurso disponible?) then (Sí)
  :Confirmar reserva;
  :Guardar en sistema;
  :Notificar al usuario;
else (No)
  :Mostrar mensaje de no disponibilidad;
endif

stop

@enduml