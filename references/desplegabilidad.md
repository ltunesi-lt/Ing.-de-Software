# DESPLEGABILIDAD (Deployability)
Fuente: `Software Architecture in Practice, 4th Edition` — Ver págs. 107-108 (General Scenario Table). Este archivo resume los valores típicos; validar contra el texto original si está disponible.

La Desplegabilidad mide qué tan fácil, rápido y seguro es llevar una nueva versión del sistema (o parte de él) a un entorno de ejecución, y revertir si algo falla.

## Valores típicos de la General Scenario Table

- **Fuente del estímulo**: desarrollador, ingeniero de release/DevOps, sistema de integración continua, pipeline automatizado.
- **Estímulo**: se solicita el despliegue de una nueva versión, un hotfix, un rollback, o un cambio de configuración.
- **Artefacto**: un componente/servicio individual, un subsistema, o el sistema completo.
- **Ambiente**: tiempo de diseño, tiempo de compilación/build, tiempo de despliegue, runtime (despliegue en caliente).
- **Respuesta**: el sistema se despliega de forma automatizada, con mínima intervención manual, sin (o con mínimo) downtime; se valida el despliegue (smoke tests); se puede revertir (rollback) si falla la validación.
- **Medida de la respuesta**: tiempo total del despliegue; porcentaje de despliegues exitosos sin intervención manual; tiempo de downtime durante el despliegue; tiempo para hacer rollback completo; cantidad de pasos manuales requeridos.


