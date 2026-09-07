# TESTEABILIDAD (Testability)
Fuente: `Software Architecture in Practice, 4th Edition` — Ver págs. 237-238 (General Scenario Table). Este archivo resume los valores típicos; validar contra el texto original si está disponible.

La Testeabilidad mide qué tan fácil es diseñar y ejecutar pruebas que revelen fallas en el sistema, y con qué facilidad se puede controlar y observar el estado interno durante las pruebas.

## Valores típicos de la General Scenario Table

- **Fuente del estímulo**: desarrollador, tester/QA, sistema de integración continua.
- **Estímulo**: se completa una unidad de código/un incremento de diseño y debe probarse; se detecta un cambio que requiere re-testear.
- **Artefacto**: unidad de código, componente, subsistema, sistema completo.
- **Ambiente**: tiempo de desarrollo, tiempo de integración continua, tiempo de diseño.
- **Respuesta**: el equipo/pipeline ejecuta pruebas que controlan las entradas y observan las salidas del componente, con capacidad de aislar el componente de sus dependencias (mocks/stubs), obteniendo cobertura suficiente para detectar la mayoría de los defectos.
- **Medida de la respuesta**: porcentaje de cobertura de código/rama alcanzado; tiempo/esfuerzo para preparar y ejecutar las pruebas; porcentaje de defectos detectados antes de producción; tiempo entre la introducción de una falla y su detección.


