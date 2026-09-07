# SEGURIDAD OPERACIONAL (Safety)
Fuente: `Software Architecture in Practice, 4th Edition` — Ver págs. 198-199 (General Scenario Table). Este archivo resume los valores típicos; validar contra el texto original si está disponible.

La Seguridad Operacional (Safety) mide la capacidad del sistema de evitar o contener condiciones que puedan causar daño físico a personas, al entorno o al propio sistema/equipamiento — distinta de "Security" (protección contra ataques intencionales).

## Valores típicos de la General Scenario Table

- **Fuente del estímulo**: el sistema mismo, un operador humano, un componente de hardware, una condición ambiental.
- **Estímulo**: se detecta una condición insegura, una falla de un componente crítico, una entrada fuera de rango operable, o una secuencia de operación peligrosa.
- **Artefacto**: componente crítico para la seguridad, sistema completo, interfaz con el entorno físico.
- **Ambiente**: operación normal, modo de emergencia, arranque/parada, mantenimiento.
- **Respuesta**: el sistema entra en un estado seguro conocido (fail-safe), detiene la operación peligrosa, alerta al operador, registra el evento para auditoría posterior, limita el daño.
- **Medida de la respuesta**: tiempo hasta alcanzar el estado seguro; probabilidad de condición insegura no detectada; tiempo de reacción del sistema ante la condición peligrosa; daño evitado/contenido (cuantificado según el dominio).


