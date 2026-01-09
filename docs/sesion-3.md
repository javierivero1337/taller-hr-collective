# Guía de Slides: Sesión 3
## Título: The AI-Augmented Interview

**Objetivo:** Estructurar datos de entrevistas: Audio -> Texto -> Scorecard.

---

### Bloque 1: Apertura (15 min)
**Slide 1: Portada**
*   *Texto:* Sesión 3: Entrevistas Aumentadas.

**Slide 2: El Proceso de Hiring: El Embudo de Decisión**
*   *Concepto:* Entender el reclutamiento como un funnel: Sourcing -> Screening -> Evaluación Técnica -> Fit Cultural -> Oferta.
*   *Falla común:* Tratar cada etapa como un juicio subjetivo en lugar de una medición objetiva.

**Slide 3: Sesgos Cognitivos: Los Enemigos del Talento**
*   *Efecto Halo/Horn:* Dejar que un rasgo (ej. dónde estudió) domine toda la evaluación.
*   *Sesgo de Afinidad:* Preferir a quienes se parecen a nosotros (mismos hobbies, misma universidad).
*   *Sesgo de Confirmación:* Pasar la entrevista buscando pruebas para validar nuestra primera impresión de los primeros 30 segundos.

**Slide 4: La Falacia de la Entrevista No Estructurada**
*   *Realidad:* La entrevista tradicional tiene una correlación bajísima con el desempeño real.
*   *El Problema:* Confiamos en nuestro "instinto" (gut feeling), que no es más que una colección de prejuicios inconscientes.
*   *Solución:* Transición hacia datos estructurados y evidencia reproducible.

---

### Bloque 2: Teoría (30 min)
**Slide 5: Pipeline de Datos**
*   *Visual:* Audio (Grabación) -> Texto (Transcripción) -> IA (Procesamiento) -> Scorecard (Decisión).
*   *Herramientas:* Mencionar Whisper, Otter, o la app móvil.

**Slide 6: El Scorecard**
*   *Concepto:* No se puede medir lo que no se define.
*   *Visual:* Ejemplo de una rúbrica mala ("Del 1 al 10") vs. buena ("Evidencias conductuales").

---

### Bloque 3: Live Demo (45 min)
**Slide 7: Paso 1 - Diseñando la Entrevista Estructurada**
*   *Acción:* Tomar la Job Description generada en la sesión anterior y transformarla en una guía de entrevista.
*   *Concepto:* No improvisar. Cada pregunta debe tener un "por qué" y un "qué espero escuchar".
*   *Prompt de ejecución:* 
    ```text
    Actúa como un Experto en Selección por Competencias. 
    Tengo esta JD: [Pegar JD]. 
    1. Identifica las 3 competencias críticas para el éxito en este rol. 
    2. Crea 2 preguntas STAR (Situación, Tarea, Acción, Resultado) por cada competencia. 
    3. Para cada pregunta, define un "Indicador de Respuesta Excelente" (qué evidencias buscamos).
    ```
*   *Meta:* Crear una hoja de ruta que elimine el sesgo de "me cayó bien".

**Slide 8: Paso 2 - Captura y Transcripción (La Magia en Vivo)**
*   *Acción:* Simular una respuesta de entrevista (2-3 min) y procesarla en tiempo real.
*   *Herramientas:* Uso de la App móvil de ChatGPT (Modo Voz), Word Dictado o Whisper.
*   *Dinámica:*
    1. El instructor pone un audio o pide a un voluntario una respuesta rápida.
    2. Se muestra cómo la IA transcribe palabra por palabra, capturando matices que el reclutador suele perder mientras toma notas.
*   *Visual:* Pantalla compartida mostrando la transcripción fluyendo en vivo.

**Slide 9: Paso 3 - Evaluación con IA (Caso Real: Operations Associate)**
*   *Acción:* Someter la transcripción a un modelo de IA configurado con principios operativos reales.
*   *Contexto de la Vacante (Nexus Ops - Anonymized):*
    > "Nexus Ops está lanzando sus Centros de Entrega Globales. Buscamos personas dinámicas para diseñar y escalar nuestras operaciones de la próxima década. Responsabilidades: Resolver problemas de usuarios, analizar procesos para escalar la operación, y colaborar con equipos de producto."
*   *Prompt Maestro (Estructura de Scorecard Real):*
    ```markdown
    Actúa como un Reclutador Senior en Nexus Ops. 
    OBJETIVO: Convertir estas notas crudas de entrevista en un scorecard legible y estructurado. 
    CRITERIO DE CORTE: No basta con comportamientos base. Buscamos alto impacto. Si el candidato no es directo o no provee evidencia clara de resultados, no debe pasar.

    EVALÚA LOS SIGUIENTES PRINCIPIOS:
    1. Delivering Outstanding Results: ¿Demostró comportamientos y mentalidad alineados con entregar resultados excepcionales? (Opciones: Strong yes, yes, no, definitely not). Apoya con evidencia corta y sucinta.
    2. Exothermic: ¿Es una persona que genera energía en el equipo? (Opciones: Strong yes, yes, no, definitely not). Apoya con evidencia.
    3. Users First: ¿Pone al usuario en el centro de sus decisiones? (Opciones: Strong yes, yes, no, definitely not). Apoya con evidencia.

    RECOMENDACIÓN FINAL: (Strong yes, yes, no, definitely not)
    KEY TAKE-AWAYS: (Conclusiones, pros, contras y temas para seguimiento).

    JOB DESCRIPTION:
    <jd>
    Nexus Ops is launching Nexus Delivery Centers - a brand new global team to design, implement and grow operations. 
    Responsibilities:
    - Troubleshoot and solve external user issues.
    - Analyze processes to scale operations and improve user experience.
    - Partner with global specialists to run critical workflows.
    Who you are:
    - User first mindset, analytical thinking, excellent communication.
    - Process-oriented and able to prioritize in quick-moving environments.
    </jd>

    TRANSCRIPCIÓN:
    [Pegar aquí el texto de la entrevista]
    ```
*   *Meta:* Mostrar cómo la IA puede aplicar "filtros de cultura y principios" de forma mucho más rigurosa que una lectura rápida humana.

---

**Slide 10: Panorama de Herramientas AI en el Mercado**
*   *Concepto:* Más allá de ChatGPT, existen soluciones especializadas para cada etapa del embudo.
*   *Herramientas Clave:*
    *   **Paradox (Olivia):** Asistente conversacional para reclutamiento masivo; automatiza screening y agendamiento vía chat.
    *   **HireEZ:** Plataforma de sourcing y outbound; utiliza agentes de IA para encontrar perfiles y automatizar el contacto inicial.
    *   **SeekOut:** Inteligencia de talento centrada en candidatos pasivos y diversidad; agrega datos de múltiples fuentes.
    *   **Eightfold AI:** Plataforma enterprise que usa Deep Learning para matching basado en skills y movilidad interna.
    *   **Juicebox (PeopleGPT):** Herramientas de sourcing conversacional; genera shortlists curados usando lenguaje natural.
    *   **Metaview:** Automatiza la toma de notas y evaluaciones de entrevistas, mejorando la calidad de las decisiones.
    *   **HireVue:** Especialista en video entrevistas y evaluaciones de habilidades con IA para reducir sesgos.
    *   **Gem:** Plataforma integral (ATS + CRM) que embebe IA en todo el flujo de trabajo de reclutamiento.
    *   **Workable:** ATS con IA para screening y distribución de vacantes, ideal para PYMEs.
    *   **Humanly:** Automatiza el engagement y las entrevistas iniciales para mejorar la eficiencia en alto volumen.

---

### Bloque 4: Hands-on / Workshop (45 min)
**Slide 11: Workshop - Tu Entrevista Aumentada (Paso 1: Diseño)**
*   *Actividad:* Diseñar el marco de evaluación para una vacante real.
*   *Instrucciones:*
    1. Toma la JD que generaste en la Sesión 2 (o una vacante actual).
    2. Identifica los 2 "Operating Principles" o Competencias más críticos para ese rol.
    3. Usa el prompt de la **Slide 7** para generar 4 preguntas STAR personalizadas.
    4. Define tu rúbrica de éxito: ¿Qué respuesta sería un "Strong Yes" y cuál un "No"?

**Slide 12: Workshop - Paso 2: Ejecución y Captura**
*   *Actividad:* Roleplay y captura de datos en tiempo real.
*   *Dinámica (En parejas):*
    1. **Entrevistador:** Elige una de tus preguntas STAR y lánzala.
    2. **Candidato:** Responde durante 2-3 minutos basándote en una experiencia real.
    3. **Captura:** El entrevistador debe usar la App de ChatGPT (Modo Voz/Dictado) o Word para transcribir la respuesta **sin interrumpir el flujo**.
*   *Tip:* Asegúrate de pedir permiso antes de "grabar/transcribir".

**Slide 13: Workshop - Paso 3: Auditoría de IA y Decisión**
*   *Actividad:* Procesar la entrevista con el Prompt Maestro y analizar resultados.
*   *Instrucciones:*
    1. Copia la transcripción obtenida en el paso anterior.
    2. Adapta el **Prompt Maestro de la Slide 9** con tu JD y tus criterios.
    3. Pide a la IA que evalúe y genere el Scorecard.
*   *Debate en Pareja:*
    *   ¿La IA detectó alguna "Red Flag" que tú pasaste por alto?
    *   ¿Las citas textuales justifican realmente la calificación dada?
    *   ¿Qué tan cerca estuvo la recomendación de la IA de tu "gut feeling"?

**Slide 14: Reflexión Grupal: ¿Datos o Instinto?**
*   *Preguntas clave:*
    *   ¿Cómo cambia la dinámica de la entrevista cuando no tienes que tomar notas desesperadamente?
    *   ¿Es este proceso más justo para el candidato?
    *   ¿Qué tan escalable es este modelo en tu organización actual?

---

### Bloque 5: Cierre (15 min)
**Slide 15: Ética del Grabado**
*   *Key Point:* Siempre pedir consentimiento. Transparencia total con el candidato.

**Slide 16: Teaser**
*   *Texto:* "Ya sabemos seleccionar. Próxima sesión: ¿Cómo definimos el éxito y el desempeño? (Competencias)."

