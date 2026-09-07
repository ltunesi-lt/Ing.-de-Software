# EFICIENCIA ENERGÉTICA (Energy Efficiency)
Fuente: `Software Architecture in Practice, 4th Edition` — Ver pág. 123 (General Scenario Table). Este archivo resume los valores típicos; validar contra el texto original si está disponible.

La Eficiencia Energética mide qué tan bien la arquitectura gestiona y minimiza el consumo de energía del hardware sobre el que corre el software, sin sacrificar de forma inaceptable otras cualidades.

## Valores típicos de la General Scenario Table

- **Fuente del estímulo**: usuario, administrador del sistema, el propio sistema (autogestión), condiciones del entorno (batería baja, temperatura).
- **Estímulo**: solicitud de reducir el consumo energético, cambio en la disponibilidad de energía (batería, corte de suministro), cambio en la carga de trabajo.
- **Artefacto**: procesador, dispositivo, componente de software, sistema completo, centro de datos.
- **Ambiente**: operación normal, modo de bajo consumo/ahorro de energía, pico de carga, alimentado por batería.
- **Respuesta**: el sistema reduce frecuencia de CPU, apaga componentes no usados, reduce polling/frecuencia de sincronización, consolida cargas de trabajo, entra en modo de bajo consumo, notifica al usuario del estado.
- **Medida de la respuesta**: consumo de energía (watts/joules) antes y después; porcentaje de reducción del consumo; tiempo de autonomía de batería resultante; impacto en performance permitido durante el modo de ahorro.


