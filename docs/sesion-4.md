# Guía de Slides: Sesión 4
## Título: Performance Architecture (Competencias)

**Objetivo:** Definir competencias y rúbricas (BARS) usando semántica.

---

### Bloque 1: Apertura (15 min)
**Slide 1: Portada**
*   *Texto:* Sesión 4: Arquitectura de Desempeño.

**Slide 2: El Estado Actual del Desempeño**
*   *Dato:* "El 95% de los managers no están satisfechos con su sistema de performance reviews (Gartner)."
*   *Realidad:* El proceso suele sentirse como un trámite administrativo, no como un motor de crecimiento.
*   *Meta:* Dejar de evaluar "personas" y empezar a evaluar "comportamientos".

**Slide 3: El Dilema del Feedback**
*   *Frase:* "Es que no tiene 'punch'...", "Le falta ponerse la camiseta" o "Es muy proactivo".
*   *El Problema:* Los adjetivos son subjetivos. Lo que para mí es "proactivo", para otro es "intrusivo".
*   *Solución:* Convertir sensaciones vagas en descripciones observables.

**Slide 4: Sesgos en la Evaluación (Los "Vampiros" del Desempeño)**
*   *Efecto de Recencia:* Evaluar al empleado por lo que hizo las últimas 2 semanas, olvidando los 6 meses anteriores.
*   *Sesgo de Leniencia/Severidad:* El manager "buena onda" que pone 5 a todos vs el manager "exigente" que no pone más de 3.
*   *Efecto Halo:* "Como es muy bueno técnicamente, asumo que también es buen líder" (aunque no lo sea).

**Slide 5: El Cambio de Paradigma: De Opiniones a Evidencias**
*   *Concepto:* Usar la IA no para que "decida" por nosotros, sino para que actúe como un **Árbitro Semántico**.
*   *Valor:* La IA nos ayuda a redactar feedback que sea:
    *   **Específico:** Basado en hechos.
    *   **Objetivo:** Comparado contra una rúbrica (BARS).
    *   **Accionable:** Con pasos claros de mejora.

---

### Bloque 2: Teoría (30 min)
**Slide 6: Semántica y Matices: La IA como Lexicógrafo**
*   **El Poder del Lenguaje**: La IA no solo "genera texto", entiende la jerarquía semántica y la intención detrás de las palabras.
*   **Diferenciación de Intensidad**: Sabe distinguir perfectamente entre "Participar", "Contribuir", "Influir" y "Liderar".
*   **Ejemplo de Matiz**:
    *   *Nivel Básico:* "Hace preguntas en las reuniones." (Pasivo/Reactivo).
    *   *Nivel Avanzado:* "Sintetiza puntos de vista divergentes para facilitar acuerdos." (Activo/Estratégico).
*   **Uso en HR**: Eliminar la ambigüedad en los diccionarios de competencias que nadie entiende.

**Slide 7: BARS (Behaviorally Anchored Rating Scales)**
*   **¿Qué es?**: Un método que sustituye los números genéricos (1 al 5) por descripciones conductuales concretas y observables.
*   **Por qué es superior**:
    *   **Objetividad**: El empleado y el manager ya no discuten por un número, sino por si el comportamiento descrito ocurrió o no.
    *   **Claridad de Carrera**: El colaborador sabe exactamente qué conducta debe mostrar para alcanzar el siguiente nivel de seniority.
*   **Visual**: Gráfico de una escalera donde cada peldaño es un comportamiento, no un adjetivo.

**Slide 8: De Adjetivos a Comportamientos (BARS en Acción)**
*   **Caso: Competencia "Resolución de Problemas"**
*   **Escala Tradicional (Mala)**:
    *   1: Insatisfactorio | 3: Cumple | 5: Excelente.
*   **Escala BARS (Buena)**:
    *   **Nivel 1 (Necesita Mejora):** "Espera a recibir instrucciones detalladas ante cualquier obstáculo; se bloquea si el proceso no está escrito."
    *   **Nivel 3 (Cumple):** "Identifica cuellos de botella antes de que escalen y propone soluciones viables basadas en datos."
    *   **Nivel 5 (Excede):** "Anticipa fallos sistémicos meses antes y rediseña los procesos para prevenir problemas en otras áreas."

**Slide 9: La Anatomía de una Competencia Aumentada**
1.  **Nombre**: Etiqueta clara (ej. Pensamiento Estratégico).
2.  **Definición**: Qué significa esto específicamente para nuestra cultura.
3.  **Dimensiones**: Sub-habilidades que la componen (ej. Análisis, Visión, Ejecución).
4.  **Rúbrica BARS**: Los niveles de dominio con ejemplos de "lo que se ve en el piso de la oficina".

---

### Bloque 3: Live Demo (45 min)
**Slide 10: Paso 1 - De la Abstracción a la Acción (Definición)**
*   *Acción:* Definir la "columna vertebral" de una competencia.
*   *Concepto:* No basta con un nombre; necesitamos dimensiones claras.
*   *Prompt de ejecución:* 
    ```text
    Actúa como un Arquitecto de Talento. 
    Define la competencia 'Propiedad (Ownership)' para una empresa de producto tech. 
    1. Describe qué significa en 2 párrafos con un tono de alto rendimiento. 
    2. Divide la competencia en 3 dimensiones: Responsabilidad Personal, Resolución Proactiva y Calidad de Entrega.
    ```

**Slide 11: Paso 2 - El Constructor de Matrices BARS**
*   *Acción:* Transformar dimensiones en comportamientos medibles.
*   *Prompt de ejecución:* 
    ```text
    Usa la competencia y dimensiones anteriores para crear una matriz BARS en tabla Markdown. 
    Columnas: Nivel 1 (En Desarrollo), Nivel 3 (Sólido/Esperado), Nivel 5 (Referente/Excede). 
    Filas: Las 3 dimensiones definidas. 
    REGLA DE ORO: Describe acciones que un manager podría 'ver' o 'oír' en una reunión o en Slack. Cero adjetivos subjetivos.
    ```

**Slide 12: Paso 3 - El Prompt Maestro (Performance Coaching)**
*   *Concepto:* Usar la rúbrica para preparar conversaciones difíciles de verdad.
*   *Prompt Maestro:*
    ```markdown
    Actúa como un Coach de Management y Experto en Feedback. 
    OBJETIVO: Preparar una sesión de performance review basada en evidencias.

    RÚBRICA DE REFERENCIA (BARS):
    [Pegar aquí la tabla generada en el paso anterior]

    HECHOS OBSERVADOS:
    - Empleado: [Nombre]
    - Situación: "Entregó el proyecto 2 días tarde, pero el código no tuvo errores y ayudó a otros 2 compañeros a terminar sus tareas."
    - Nivel esperado para su rol: Nivel 3.

    TAREA:
    1. ANÁLISIS: Según la rúbrica, ¿en qué nivel está operando hoy este empleado en cada dimensión? Justifica con los hechos.
    2. FEEDBACK COIN: Redacta un script de conversación siguiendo:
       - Contexto: El momento específico.
       - Observación: El hecho objetivo (sin juicios).
       - Impacto: Cómo afectó al equipo/negocio.
       - Next Steps: Qué necesita hacer para llegar al Nivel 5.
    3. PREPARACIÓN: Anticipa 2 objeciones del empleado y dame respuestas empáticas pero alineadas a la rúbrica.
    ```
*   *Meta:* Mostrar que la IA no evalúa, sino que organiza el pensamiento del manager para una conversación más justa.

**Slide 13: Bonus Track - El Performance Review Formal (Anual/Semestral)**
*   *Concepto:* Cuando llega el "Día del Juicio" (Review Anual), el manager suele estar abrumado por múltiples fuentes de datos.
*   *Solución:* Usar un prompt estructurado que integre Feedback de Pares, Autoevaluación y Notas del Manager para generar un reporte balanceado.
*   *Caso de Uso:* "Scarlett", una empleada de alto rendimiento previo que está luchando con la adaptación a un nuevo equipo (Ego vs. Colaboración).
*   *Prompt Maestro para Performance Reviews:*
    ```markdown
    You’ll help me build an End of Year Review for my team. As a manager, I have feedback I’ve written, my team's self-assessments, and peer feedback.
    
    GOAL: Write a concise End of Year Review for [Employee Name].
    PRIORITY: Focus on behaviors repeated across feedbacks, prioritizing my manager notes.
    
    <output_format>
    Looking Back:
    - Succinctly share key accomplishments and challenge areas.
    - Share 2-3 brief examples of how this employee modeled our Operating Principles.
    
    Looking Forward:
    - List two new behaviors or skills to focus on.
    - Explain how these would make them more effective.
    </output_format>
    
    <context_operating_principles>
    [Insert Company Principles: e.g., Users First, Move with Urgency, Collaborate Egolessly, Stay Curious...]
    </context_operating_principles>
    
    <rating>
    Successfully Meet Expectations (Private rating for context)
    </rating>
    
    <peer_feedback>
    - Strength: Commitment to Quality.
    - Strength: Efficient Execution.
    - Opportunity: Collaboration & Delegation (needs to delegate more).
    </peer_feedback>
    
    <self_review>
    - Claims to "User First" by fixing login flows.
    - Claims "Curiosity" by learning Treasury products.
    - Plans to transition to Consumer Ops but wants to balance teaching with learning.
    </self_review>
    
    <past_manager_review>
    - Previous top performer (SME rating).
    - Won awards for efficiency and NPI leadership.
    - History of needing coaching on autonomy.
    </past_manager_review>
    
    <current_manager_raw_thoughts>
    [Employee] is energized but her ideas are often misaligned with our current reality. She needs to master the basics of the new operation before trying to change it. She reacts defensively when ideas are rejected (Ego). She feels the need to prove herself due to tenure, but it's counterproductive. I want to assign her to QA Calibrations to ground her in fundamentals.
    </current_manager_raw_thoughts>
    ```


---

### Bloque 4: Hands-on / Workshop (45 min)
**Slide 14: Workshop Parte 1 - Arquitectura de la Competencia (Diseño)**
*   *Actividad:* Seleccionar una competencia "crítica" y definir sus niveles BARS usando Context Stacking.
*   *Instrucciones:*
    1. Elige una competencia que hoy sea "gris" o subjetiva en tu equipo.
    2. Usa etiquetas XML para dar contexto a la IA.
*   *Prompt Sugerido:*
    ```text
    <contexto_equipo> [Ej: Equipo de Customer Success en una Startup] </contexto_equipo>
    <competencia> [Ej: Comunicación con Clientes Difíciles] </competencia>
    <instruccion> 
    Genera una matriz BARS de 3 niveles (1, 3, 5). 
    Asegúrate de que el Nivel 5 refleje a un referente en el mercado y el Nivel 1 sea un punto de acción inmediato.
    </instruccion>
    ```

**Slide 15: Workshop Parte 2 - El Simulador de Feedback (Roleplay)**
*   *Actividad:* Roleplay interactivo con la IA para practicar la entrega de feedback.
*   *Dinámica:* 
    1. Usa el **Prompt Maestro de la Slide 12** para generar tu script COIN.
    2. Configura a la IA como tu "interlocutor difícil".
*   *Prompt del Simulador:*
    ```text
    Actúa como un empleado con perfil [Ej: Senior con mucha experiencia pero resistente al cambio]. 
    Acabo de darte el siguiente feedback: [Pegar tu script COIN]. 
    Respóndeme con una objeción que pondría a prueba mi liderazgo. 
    Mantengamos el diálogo turno a turno. Mi objetivo es reconducir la charla hacia la rúbrica BARS.
    ```

**Slide 17: Workshop Parte 3 - El "End of Year Review" Challenge**
*   *Actividad:* Redactar una evaluación de desempeño completa integrando múltiples fuentes de datos.
*   *Dinámica:*
    1. Piensa en un miembro de tu equipo (o usa un caso hipotético).
    2. Recopila mentalmente (o escribe notas rápidas):
        *   Su autoevaluación (¿Qué cree que hizo bien?).
        *   Feedback de pares (¿Qué dicen otros?).
        *   Tus notas como manager (La realidad cruda).
    3. Usa el **Prompt Maestro de la Slide 13** para generar el review final.
*   *Prompt Simplificado para el Taller:*
    ```text
    Actúa como un Manager Senior. Redacta el Performance Review de fin de año para [Nombre].
    
    INPUTS:
    - Mis notas: [Ej: Gran capacidad técnica, pero le cuesta comunicar malas noticias a tiempo].
    - Feedback de pares: [Ej: Es muy colaborativo, siempre ayuda a desbloquear a otros].
    - Autoevaluación: [Ej: Cree que está listo para ascender a Senior].
    
    OUTPUT:
    Genera un texto narrativo de 2 párrafos: "Mirando hacia atrás" (Logros) y "Mirando hacia adelante" (Áreas de foco).
    ```

**Slide 18: Workshop Parte 4 - Auditoría de Equidad y Sesgos**
*   *Actividad:* Revisar el feedback y la rúbrica para asegurar que sean 100% profesionales y objetivos.
*   *Prompt Sugerido:*
    ```text
    Analiza este feedback que redacté: [Pegar feedback]. 
    1. Identifica adjetivos subjetivos y cámbialos por comportamientos observables. 
    2. ¿Detectas señales de sesgo (género, edad, cultura)? 
    3. Dame una versión final que sea 'Bias-Free' y centrada en el crecimiento.
    ```

**Slide 19: Reflexión: De Juez a Coach**
*   *Pregunta:* ¿Cómo cambia tu seguridad como manager cuando la discusión no es sobre tu "opinión" sino sobre la "rúbrica" y los datos consolidados?
*   *Key Takeaway:* La IA nos ayuda a separar a la persona del comportamiento y a ver la "película completa" del año.

---

### Bloque 5: Cierre (15 min)
**Slide 20: El Valor de la Claridad**
*   *Reflexión:* La claridad es amabilidad. La IA nos ayuda a ser claros para que el empleado pueda ganar.

**Slide 21: Teaser**
*   *Texto:* "Última sesión: Escuchar a todos a la vez. (Clima, Cultura y Análisis de Sentimiento)."

