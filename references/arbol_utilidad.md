---
name: arbol-de-utilidad
description: usarla el usuario quiere crear un arbol de utilidad completo
---
# ARBOL DE UTILIDAD (UTILITY TREE)

## Propósito
El Árbol de Utilidad permite estructurar, descomponer y priorizar los Requisitos No Funcionales (Atributos de Calidad) del sistema partiendo de la "Utilidad" general hasta llegar a escenarios concretos y medibles.

## Estructura Jerárquica del Árbol
El árbol debe estructurarse obligatoriamente en 4 niveles de profundidad:

1. Nodo Raíz: "Utilidad" (Representa la calidad general del sistema).
2. Atributos de Calidad: Los atributos relevantes identificados (ej. Disponibilidad, Performance, Seguridad).
3. Sub-atributos / Categorías: Aspectos específicos del atributo (ej. para Performance: Latencia, Throughput; para Disponibilidad: Detección de fallas, Recuperación).
4. Escenarios Específicos: Escenarios concretos vinculados al atributo, acompañados de su **Priorización (H, M, L)**.

---

## Matriz de Priorización de Escenarios (Puntuación)
Cada escenario hoja del Árbol de Utilidad debe ser evaluado y etiquetado con un par `(Importancia para el Negocio, Dificultad Arquitectónica)` utilizando los valores **High (H)**, **Medium (M)** o **Low (L)**:

* **Importancia para el Negocio (Business Value):** Determinado por el stakeholder o impacto directo en el dominio.
* **Dificultad Arquitectónica (Architectural Impact/Risk):** Esfuerzo, riesgo técnico o complejidad para la arquitectura al intentar satisfacer el escenario.

*Ejemplo de notación:* **(H, M)** = Alta importancia para el negocio, Mediana dificultad técnica.

---

## INSTRUCCIONES PARA GENERAR EL ÁRBOL
Cuando el usuario solicite un Árbol de Utilidad:

1. Lee los archivos `.md` correspondientes de `./mi_proyecto/atrib_calidad/` para los atributos identificados.
2. Identifica los sub-atributos o áreas de interés de cada uno.
3. Asocia los escenarios de calidad creados a sus respectivos sub-atributos.
4. Asigna la tupla de priorización `(Importancia, Dificultad)` a cada escenario.
5. Renderiza el resultado utilizando una estructura de árbol en formato **Markdown list** o **Tabla**.

## TAXONOMÍA DE ATRIBUTOS DE CALIDAD (BCK12)
Fuente: Keeling, *Software Architecture in Practice*, p.51.

Antes de señalar "falta la rama de X" en un árbol de utilidad existente, 
clasificar la cobertura actual contra esta taxonomía de tres franjas:

| Franja | Atributos típicos |
|---|---|
| **Design Time** | Modificabilidad, Mantenibilidad, Reusabilidad, Testeabilidad, Buildability |
| **Runtime** | Disponibilidad, Confiabilidad, Performance, Escalabilidad, Seguridad |
| **Conceptual** | Manejabilidad (Manageability), Soportabilidad, Simplicidad |

Procedimiento:
1. Marcar qué franjas están representadas en el árbol actual y con qué peso.
2. Antes de declarar "falta X", justificar por qué esa franja es relevante 
   al contexto del sistema — no basta con notar la ausencia, hay que argumentar 
   la relevancia contra el enunciado del stakeholder (ej. un sistema en 
   migración activa tiene fuerte razón arquitectónica para necesitar cobertura 
   de Modificabilidad/Testeabilidad — franja Design Time — más allá de si el 
   stakeholder la mencionó explícitamente).
3. Reportar la cobertura como una matriz franja → presente/ausente/débil, 
   no como una lista suelta de "atributos que faltan".
## VALIDACIÓN DE PRIORIDAD CONTRA BUSINESS GOALS
Fuente: Keeling, *Software Architecture in Practice*, cap. 4, p.43-45.

Antes de asignar la tupla (Importancia, Dificultad) a un escenario:

1. Extraer del enunciado del stakeholder los business goals explícitos o 
   implícitos, y formalizarlos en formato **Subject / Outcome / Context** 
   (ej. Subject: "el sistema de pagos", Outcome: "debe estar disponible", 
   Context: "porque una caída cuesta ingresos por segundo").
2. Cada tupla de prioridad debe citar contra qué business goal se está 
   evaluando — no asignarse por intuición arquitectónica aunque el resultado 
   "parezca" correcto.
3. Formato de reporte por escenario:
   `(H, H) — Business goal: [Subject/Outcome/Context] → cita textual o 
   paráfrasis de la frase del stakeholder que lo sostiene`.
4. Si un escenario recibe prioridad alta pero no hay un business goal 
   identificable que lo sostenga, marcarlo como **prioridad no trazada** 
   y flaggearlo para validar con el stakeholder antes de tratarlo como 
   definitivo — no queda "así nomás" en el árbol.
5. La distinción must-have / nice-to-have se decide en función de esta 
   trazabilidad, no de la dificultad técnica percibida.
