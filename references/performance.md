# PERFORMANCE
Fuente: `Software Architecture in Practice, 4th Edition` — Ver págs. 175-176 (General Scenario Table). Este archivo resume los valores típicos; validar contra el texto original si está disponible.

La Performance mide la capacidad del sistema de responder a eventos (solicitudes de usuario, mensajes, eventos internos) dentro de restricciones de tiempo o volumen aceptables.

## Valores típicos de la General Scenario Table

- **Fuente del estímulo**: uno o varios usuarios, sistemas externos, componentes internos del sistema.
- **Estímulo**: llegada de un evento — solicitud periódica, esporádica o aleatoria; ráfaga de eventos (burst); carga sostenida.
- **Artefacto**: sistema completo, servicio específico, componente individual.
- **Ambiente**: operación normal, sobrecarga (peak load), modo de emergencia/degradado.
- **Respuesta**: el sistema procesa el/los evento(s) y produce la salida correspondiente, posiblemente con cambios de prioridad, cambio en el nivel de servicio, o consumo de recursos.
- **Medida de la respuesta**: latencia (tiempo de respuesta) promedio/percentil (p95, p99); throughput (transacciones/segundo); jitter (variabilidad de latencia); tasa de eventos perdidos o rechazados bajo carga.


