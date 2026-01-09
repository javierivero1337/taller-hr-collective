# Guía de Slides: Sesión 2
## Título: Strategic Talent Acquisition (Deep Research)

**Objetivo:** Usar Deep Research para investigar mercado y crear JDs estratégicas.

---

### Bloque 1: Apertura (15 min)
**Slide 1: Portada**
*   *Texto:* Sesión 2: Atracción de Talento Estratégica.

**Slide 2: El Problema de Hoy**
*   *Dato:* "El 80% de las JDs son 'copiar-pegar' de hace 5 años".
*   *Meta:* Dejar de pedir "lo de siempre" y empezar a pedir "lo que el mercado tiene".

---

### Bloque 2: Teoría (30 min)
**Slide 3: Deep Research - El Poder de la Investigación Autónoma**
*   **¿Qué es Deep Research?**: Es un modelo de IA configurado como "agente" que no solo responde preguntas, sino que ejecuta un proceso de investigación completo:
    *   **Navegación Iterativa**: Realiza decenas de búsquedas, "lee" múltiples sitios web, descarta información irrelevante y profundiza en fuentes clave.
    *   **Razonamiento y Planificación**: Antes de buscar, la IA diseña un plan de qué investigar. Si encuentra algo nuevo, ajusta su plan en tiempo real.
    *   **Síntesis Multi-fuente**: Consolida información de fuentes técnicas, noticias, foros y documentos oficiales en un solo reporte estructurado.
*   **Deep Research vs. Chat Normal (LLM Tradicional)**:
    *   **Chat Normal**: Está optimizado para la velocidad. Da respuestas basadas mayormente en su entrenamiento previo o una búsqueda superficial (1-3 links). Es ideal para tareas rápidas y creativas.
    *   **Deep Research**: Está optimizado para la profundidad y precisión. Puede tardar minutos en lugar de segundos porque está "trabajando" por ti. Es ideal para análisis de mercado, comparativas técnicas y validación de hechos.
*   **Deep Research vs. Google**: Google te entrega una lista de links (tú haces el trabajo). Deep Research te entrega la conclusión y el reporte (la IA hace el trabajo).
*   **Visual**: Gráfico comparativo: Búsqueda tradicional (lista de links) vs. Chat Normal (Respuesta directa) vs. Deep Research (Reporte consolidado con fuentes).

**Slide 4: Context Stacking & Candidate Persona (El Core de la JD)**
*   **Técnica: Apilar capas de información estratégica**: No podemos pedirle a la IA que cree una JD sin darle el contexto profundo de la empresa y del humano que buscamos. 
    *   **Capa 1: ADN y Desafíos de la Empresa**:
        *   *¿Qué incluir?*: Cultura, retos actuales (ej. migración a la nube, expansión a Latam), y por qué el puesto está abierto hoy.
        *   *Ejemplo*: "Somos una Fintech escalando de 10 a 50 ingenieros. El reto es mantener la agilidad sin romper la arquitectura legacy mientras integramos IA en el core."
    *   **Capa 2: Datos de Mercado (Deep Research)**:
        *   *¿Qué incluir?*: Salarios reales, beneficios que la competencia ofrece y escasez de talento.
        *   *Ejemplo*: "Los Senior Devs en CDMX hoy buscan esquemas 100% remotos y bonos por desempeño. Nuestra oferta debe ser competitiva contra gigantes como Nubank o Mercado Libre."
    *   **Capa 3: El Perfil Psicográfico (Candidate Persona)**:
        *   *¿Qué incluir?*: Motivaciones, frustraciones y hábitos del candidato ideal.
        *   *Ejemplo*: "Buscamos a alguien que lea HackerNews, que le frustre la burocracia corporativa y que valore la autonomía radical sobre el prestigio de la marca."

**Slide 5: Diseñando el Prompt Maestro (Deep Research Mode)**
*   **Concepto**: El prompt no es una simple orden, es una **misión de investigación completa**.
*   **Ejemplo de Prompt de Deep Research para una JD**:
    ```markdown
    Actúa como un Consultor de Estrategia de Talento e IA Senior. 
    MI OBJETIVO: Construir un reporte de mercado y el perfil ideal para un [Nombre del Rol].
    
    PASO 1: INVESTIGACIÓN DE MERCADO (Deep Research)
    - Analiza las JDs de [Competidor A] y [Competidor B] para roles similares. ¿Qué 'ganchos' están usando?
    - Identifica las 3 habilidades técnicas más demandadas y las 2 más difíciles de encontrar para este perfil en 2024.
    - Encuentra rangos salariales reales (no solo promedios) para [Ubicación] en percentiles 50, 75 y 90.
    
    PASO 2: CONTEXTO DE LA EMPRESA (Capa 1)
    - Tenemos estos retos: [Describir retos, ej: deuda técnica, expansión rápida, cambio de cultura].
    - ¿Cómo debería este rol ayudar a resolver estos problemas específicos?
    
    PASO 3: DEFINICIÓN DEL CANDIDATE PERSONA (Capa 3)
    - Basado en lo anterior, define: ¿Qué le duele a este candidato en su trabajo actual? ¿Qué le haría decir 'sí' a nuestra propuesta sin dudarlo?
    
    ENTREGABLE: Un reporte estratégico que servirá de base para redactar la JD final.
    ```

---

### Bloque 3: Live Demo (45 min)
**Slide 6: Paso 1 - Investigación en Tiempo Real (Deep Research)**
*   *Acción:* Ejecutar la fase de "Discovery" usando el primer bloque del Prompt Maestro.
*   *Prompt de ejecución:* 
    ```text
    Analiza el mercado de [Data Scientist] en [CDMX/Remoto]. 
    1. Compara las propuestas de valor de [Empresa A] y [Empresa B]. 
    2. Identifica los 3 'skills' técnicos más escasos según foros y tendencias de 2024.
    3. Busca rangos salariales reales por percentiles.
    ```
*   *Meta:* Obtener la materia prima para la "Capa 2" del Context Stacking.

**Slide 7: Paso 2 y 3 - Contexto y Candidate Persona**
*   *Acción:* Integrar los desafíos de la empresa (Capa 1) con los hallazgos del mercado para definir al humano ideal.
*   *Prompt de ejecución:* 
    ```text
    Con los datos de mercado anteriores y sabiendo que nuestro reto es [Ej: escalar de 10 a 50 ingenieros sin perder agilidad]:
    1. Define el perfil psicográfico (Motivaciones y Frustraciones).
    2. ¿Qué 'gancho' conectaría emocionalmente con este candidato?
    3. Crea un resumen del 'Candidate Persona' que incluya sus hábitos (ej. qué lee, qué valora).
    ```
*   *Meta:* Crear un perfil que no se base en requisitos, sino en motivaciones.

**Slide 8: El Entregable - Redacción de la JD "Out of the Box"**
*   *Acción:* Consolidar todo el "Context Stacking" en una descripción de puesto disruptiva.
*   *Prompt de ejecución:* 
    ```text
    Actúa como un Copywriter de Employer Branding. 
    Usa toda la información (Mercado + Contexto + Persona) para redactar la JD final.
    - Tono: Innovador y desafiante. 
    - Estructura: 'Tu Misión', 'Tus Retos', 'Tus Beneficios'. 
    - Regla de Oro: Prohibido usar la palabra 'Requisitos' o 'Requerimientos'.
    ```
*   *Meta:* Pasar del reporte estratégico a una pieza de atracción de talento real.

---

### Bloque 4: Hands-on / Workshop (45 min)
**Slide 9: Challenge: La Vacante Imposible**
*   *Instrucción:* Elige esa vacante que llevas meses sin poder cerrar o una posición nueva y compleja.
*   *Metodología:* Vamos a aplicar el **Prompt Maestro** en 3 fases usando **XML Tags** para organizar el contexto.

**Slide 10: Fase 1 - Deep Research (Mercado)**
*   *Actividad:* Ejecuta la investigación de mercado y competidores.
*   *Prompt Sugerido:* 
    ```text
    <investigacion_mercado>
    Analiza tendencias salariales, skills emergentes y qué están ofreciendo los competidores para el rol de [Nombre del Rol] en [Ubicación]. Identifica qué ganchos están usando.
    </investigacion_mercado>
    ```

**Slide 11: Fase 2 - Context Stacking (Empresa + Persona)**
*   *Actividad:* Añade tu contexto y crea el perfil psicográfico.
*   *Estructura:*
    ```text
    <contexto_empresa> [Escribe aquí tu reto: ej. cambio de cultura, expansión, deuda técnica] </contexto_empresa>
    <instruccion> 
    Basado en la investigación de mercado previa y mi contexto, define el Candidate Persona: Motivaciones, dolores y por qué nos elegirían.
    </instruccion>
    ```

**Slide 12: Fase 3 - Drafting & Audit (La JD Final)**
*   *Actividad:* Genera la JD y hazle una auditoría de sesgos.
*   *Prompt Sugerido:* 
    ```text
    <instruccion_redaccion> 
    Redacta la JD con estructura 'Misión/Retos/Beneficios'. Tono retador. Sin usar la palabra 'Requisitos'. 
    </instruccion_redaccion>
    
    <auditoria>
    Analiza la JD anterior. ¿Tiene sesgos de género? ¿Es demasiado corporativa? Sugiéreme 3 mejoras.
    </auditoria>
    ```

---

### Bloque 5: Cierre (15 min)
**Slide 13: Galería de JDs**
*   *Dinámica:* Leer en voz alta los "Job Titles" creativos que salieron.

**Slide 14: Next Steps**
*   *Texto:* "Ya tenemos el QUÉ buscamos. En la próxima sesión veremos CÓMO lo evaluamos (Entrevistas)."

