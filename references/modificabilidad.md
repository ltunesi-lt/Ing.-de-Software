# MODIFICABILIDAD (Modifiability)
Fuente: `Software Architecture in Practice, 4th Edition` — Ver pág. 158 (General Scenario Table). Este archivo resume los valores típicos; validar contra el texto original si está disponible.

La Modificabilidad mide el costo (tiempo, esfuerzo, riesgo) de realizar un cambio en el sistema: agregar, modificar o remover funcionalidad.

## Valores típicos de la General Scenario Table

- **Fuente del estímulo**: desarrollador, administrador, usuario final, product owner.
- **Estímulo**: solicitud de agregar/eliminar/modificar una funcionalidad, cambiar una cualidad de calidad, adaptar el sistema al entorno, o reemplazar una tecnología/dependencia.
- **Artefacto**: código, componentes, datos, interfaces, configuración del sistema.
- **Ambiente**: tiempo de diseño, tiempo de compilación, tiempo de build, tiempo de despliegue, runtime (configuración dinámica).
- **Respuesta**: el equipo localiza los puntos de cambio, implementa el cambio, prueba el cambio y lo despliega sin efectos colaterales imprevistos en otras partes del sistema.
- **Medida de la respuesta**: costo del cambio en tiempo/esfuerzo (horas, días-persona); cantidad de componentes/módulos afectados; cantidad de defectos introducidos; costo/riesgo relativo comparado a una línea base.


