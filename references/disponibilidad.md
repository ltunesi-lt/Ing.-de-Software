# DISPONIBILIDAD (Availability)
Fuente: `Software Architecture in Practice, 4th Edition` — Ver págs. 75-76 (General Scenario Table). Este archivo resume los valores típicos; validar contra el texto original si está disponible.

La Disponibilidad mide la proporción de tiempo que el sistema está operativo y responde correctamente, y qué tan bien tolera y se recupera de fallas.

## Valores típicos de la General Scenario Table

- **Fuente del estímulo**: personas internas/externas, hardware, software, infraestructura física (energía, red, hardware de terceros).
- **Estímulo**: falla — omisión (el componente no responde), crash, timing (respuesta tardía), respuesta incorrecta, o estado inconsistente detectado.
- **Artefacto**: procesador(es), almacenamiento, procesos/hilos, canal de comunicación (conectividad), sistema completo.
- **Ambiente**: operación normal, arranque/startup, modo degradado, sobrecarga, redundancia activa.
- **Respuesta**: el sistema debe detectar el evento (logging, notificación, monitoreo, heartbeat), prevenirlo de ser posible, recuperarse (failover, retry, degradación elegante, restart, rollback, checkpoint/rollback), y/o notificar a operadores/usuarios.
- **Medida de la respuesta**: tiempo/duración en que el sistema debe permanecer disponible; tiempo de detección de la falla; tiempo de reparación/recuperación (MTTR); intervalo entre fallas (MTBF); disponibilidad expresada como porcentaje (ej. 99.9%); duración permitida en modo degradado.


