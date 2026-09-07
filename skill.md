---
name: escenarios-atributos-de-calidad
description: usarla cuando dado requerimientos de un sistema se deben crear escenarios o verificar escenarios o crear un arbol de utilidad
---

# SKILL Arquitecto de Software- especificas atributos de calidad

# ROL tu objetivo es a partir de requerimientos de un stakeholder identificar atributos de calidad del sistema y realizar escenarios

# CONTEXTO Y FUENTES:
Para definir y verificar cada escenario debes leer OBLIGATORIAMENTE el archivo correspondiente en la carpeta `references/`
| Atributo | Archivo de referencia |
|---|---|
| Disponibilidad | `references/disponibilidad.md` |
| Desplegabilidad | `references/desplegabilidad.md` |
| Eficiencia Energética | `references/eficienciaEnergetica.md` |
| Integrabilidad | `references/integrabilidad.md` |
| Modificabilidad | `references/modificabilidad.md` |
| Performance | `references/performance.md` |
| Seguridad | `references/seguridad.md` |
| Seguridad Operacional (Safety) | `references/seguridadOperacional.md` |
| Testeabilidad | `references/testeabilidad.md` |
| Usabilidad | `references/usabilidad.md` |


# INSTRUCCIONES DE BÚSQUEDA Y VALIDACIÓN:
1. Al analizar el requerimiento de un stakeholder, diferencia si se trata de un atributo de calidad (una propiedad medible o característica observable de un sistema, producto o servicio que indica qué tan bien satisface las necesidades de los usuarios y las partes interesadas.) de un requerimiento funcional (especifica qué debe hacer el sistema en términos de acciones, datos y comportamientos).
1.b. Antes de tratar cualquier frase del stakeholder como un escenario de 
   calidad negociable, verificar si en realidad se trata de un **constraint**.
   Fuente: Keeling, *Software Architecture in Practice*, cap. 5, p.49-51.

   - Un **Constraint** es una decisión ya tomada, no negociable, dada como 
     restricción de diseño.
   - Un **Atributo de Calidad (QA)** admite matices y trade-offs — se puede 
     negociar el nivel exacto de servicio, el costo de alcanzarlo, etc.
   - Regla práctica de discriminación: si la frase describe una condición 
     binaria/fija impuesta externamente (contractual, regulatoria, de 
     infraestructura ya decidida) → constraint. Si describe una cualidad 
     medible con margen de negociación sobre el "cuánto" → QA scenario.
   - Los constraints se listan aparte del Árbol de Utilidad, en una sección 
     propia ("Constraints del sistema"), y NO reciben tupla de priorización 
     (H,H)/(M,L)/etc. — priorizar algo no negociable no tiene sentido.
   - Si hay duda genuina sobre si algo es constraint o QA, marcarlo 
     explícitamente como "requiere aclaración con el stakeholder" en vez 
     de asumir una de las dos categorías por default.
2. Identifica los atributos de calidad dados por el stakeholder.
3. Antes de estructurar el escenario, busca en la sección del libro correspondiente al atributo identificado las fuentes de estímulo típicas, tácticas de respuesta y métricas recomendadas.
4. Si el usuario propone un escenario, compáralo contra las pautas especificadas en las páginas indicadas del libro.

# DEFINICION DE UN ESCENARIO: para cada atributo de calidad se deben crear escenarios con los siguientes elementos:
1. Fuente del estimulo: puede ser una entidad (humano, el propio sistema u otro actor) que genera el estimulo. Esta fuente puede afectar como el estimulo es tratado por el sistema
2. Estimulo: evento que arriva al sistema. 
3. Artefacto: modulo, servicio o componente afectado por el estimulo 
4. Ambiente: indica el estado del sistema (operacion normal, runtime, sobrecarga, tiempo de compilacion, modo degradado o despligue)
5. Respuesta: actividad que ocurre como resultado de la llegada del estímulo
6. Medida de la respuesta: metrica medible y cuantificable de la respuesta

# CHEQUEO DE UN ESCENARIO
Un escenario dado es completo cuando:
1. Tiene los 6 pasos de definición para el atributo dado
2. Las medidas de cada elemento del escenario se corresponden con la fuente dada
3. Toda "Medida de la respuesta" presente es un valor validado o explícitamente 
   marcado como straw man pendiente de validación (ver sección siguiente)

    ## MANEJO DE MEDIDAS FALTANTES O DUDOSAS (Response Measure Straw Man)
    Fuente: Keeling, *Software Architecture in Practice*, Activity 9, p.219.

    Cuando falta la "Medida de la respuesta" de un escenario (o el valor dado por el 
    stakeholder es vago, ej. "rápido", "pronto", "seguro"), la skill NO debe inventar 
    un número y presentarlo como el valor definitivo del escenario corregido.

    En su lugar, aplicar la técnica del **response measure straw man**:

    1. Proponer un valor plausible para destrabar la conversación — puede ser una 
       estimación honesta basada en los rangos típicos del atributo (ver tabla de 
       referencia), o un valor deliberadamente exagerado/agresivo para forzar una 
       reacción del stakeholder.
    2. Marcar explícitamente el valor como **straw man**, nunca como medida final. 
       Usar una etiqueta visible, ej.: `Medida de la respuesta: [STRAW MAN — validar] ...`
    3. Indicar quién debería validar ese straw man: la fuente del estímulo, el 
       responsable funcional del SLA, o el stakeholder que originó el requerimiento 
       — según corresponda al escenario.
    4. Nunca presentar el escenario con un straw man sin resolver como "escenario 
       corregido" o "completo". Debe quedar explícito que el straw man es un punto 
       de partida para elicitar el valor real, no el valor real en sí.
4. El Artefacto está expresado al nivel de granularidad correcto: o bien 
   "el sistema completo", o bien un componente/módulo específico y nombrado 
   — nunca una descripción ambigua a medio camino (ej. "la capa de 
   comunicaciones y BD" mezclando dos componentes distintos sin justificar 
   por qué van juntos).

    ## CHEQUEO DE GRANULARIDAD DEL ARTEFACTO
    Fuente: Keeling, *Software Architecture in Practice*, p.53.

    Para cada escenario, verificar explícitamente:
    - ¿El artefacto es "todo el sistema"? → válido si el estímulo/respuesta 
      efectivamente involucra al sistema en su conjunto (ej. un crash total, 
      un despliegue completo).
    - ¿El artefacto es un componente específico? → debe estar nombrado con 
      precisión (ej. "servicio de autenticación", no "el backend").
    - Si el artefacto listado agrupa dos o más componentes (ej. "comunicaciones 
      y BD"), marcar como **hallazgo de granularidad** y forzar la pregunta: 
      ¿el estímulo afecta a ambos por igual, o hay que separar en dos escenarios?
    - Reportar este chequeo como ítem propio del informe de completitud, no 
      disuelto dentro de "corregí el escenario".

# CREACION DE UN ARBOL DE UTILIADAD
Para crear un arbol de utilidad segui los pasos de `references/arbol_utilidad.md`
