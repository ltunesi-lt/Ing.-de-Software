# INTEGRABILIDAD (Integrability)
Fuente: `Software Architecture in Practice, 4th Edition` — Ver págs. 138-139 (General Scenario Table). Este archivo resume los valores típicos; validar contra el texto original si está disponible.

La Integrabilidad mide qué tan fácil es hacer que los componentes del sistema trabajen correctamente entre sí y con sistemas/componentes externos.

## Valores típicos de la General Scenario Table

- **Fuente del estímulo**: desarrollador, integrador de sistemas, sistema externo nuevo a integrar.
- **Estímulo**: se necesita integrar un nuevo componente/servicio, cambiar una interfaz existente, o conectar con un sistema de terceros.
- **Artefacto**: componentes a integrar, interfaces/contratos (APIs), mecanismos de intercambio de información.
- **Ambiente**: tiempo de diseño, tiempo de desarrollo, tiempo de integración/build.
- **Respuesta**: el equipo integra el nuevo componente reutilizando interfaces estándar/contratos existentes, sin modificar componentes ya integrados, o con cambios acotados y documentados.
- **Medida de la respuesta**: esfuerzo (horas/días-persona) para completar la integración; cantidad de componentes existentes que debieron modificarse; cantidad de defectos introducidos durante la integración; tiempo hasta que la integración pasa las pruebas.


