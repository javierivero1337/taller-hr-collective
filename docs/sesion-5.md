# Guía de Slides: Sesión 5
## Título: Voice of the Employee (Cultura)

**Objetivo:** Análisis de sentimiento y encuestas a escala.

---

### Bloque 1: Apertura (15 min)
**Slide 1: Portada**
*   *Texto:* Sesión 5: Voz del Empleado y Cultura (Analytics & Sentiment).

**Slide 2: La Brecha del Compromiso (The Engagement Gap)**
*   *Dato:* "El 80% de las empresas mide el engagement, pero solo el 20% toma acciones que los empleados perciben."
*   *El Problema:* Las encuestas anuales son autopsias. Llegan tarde.
*   *El Dolor:* Tenemos 1,000 comentarios abiertos. Leerlos toma semanas. Entenderlos toma meses. Accionar toma años.

**Slide 3: El "Agujero Negro" de la Data Cualitativa**
*   *Situación:* RRHH ama los gráficos (Quantitative), pero ignora los comentarios de texto (Qualitative) por falta de tiempo.
*   *Riesgo:* En el texto libre es donde están las señales tempranas de renuncia (Burnout, Toxicidad, Acoso).
*   *Solución:* Usar IA para "escuchar" a escala masiva en segundos, no semanas.

---

### Bloque 2: Teoría (30 min)
**Slide 4: Más allá del Word Cloud (Nube de Palabras)**
*   *Crítica:* Las nubes de palabras no sirven. Que la palabra "Salario" sea grande no nos dice si la gente está feliz o furiosa con él.
*   *Concepto 1: Análisis de Sentimiento*: La IA clasifica la "temperatura" emocional de un texto (Positivo, Negativo, Neutro, Mixto).
*   *Concepto 2: Topic Modeling (Modelado de Temas)*: La IA agrupa comentarios dispares bajo etiquetas inteligentes (ej. "Balance Vida-Trabajo", "Liderazgo Directivo", "Herramientas de Trabajo").

**Slide 5: Privacidad y Ética (El "Must-Have")**
*   *Regla de Oro:* **Zero PII (Personally Identifiable Information)**.
*   *Protocolo de Seguridad:*
    1.  Eliminar columnas de Nombres, Emails, IDs.
    2.  Buscar/Reemplazar nombres de jefes específicos en los comentarios.
    3.  Opt-out de usar datos para entrenamiento (Configuración de privacidad en ChatGPT Team/Enterprise).

**Slide 6: La Pirámide de la Acción**
*   *Base:* Datos Crudos (Encuestas).
*   *Medio:* Insights (Lo que la IA nos dice).
*   *Cima:* Decisiones (Lo que RRHH hace).
*   *Mensaje:* La IA nos lleva de la Base al Medio instantáneamente para que nosotros pasemos el 100% del tiempo en la Cima.

---

### Bloque 3: Live Demo (45 min)
**Slide 7: Paso 1 - Diseñando la Encuesta Perfecta (Pre-Medición)**
*   *Concepto:* No empieces por las preguntas, empieza por el objetivo.
*   *Factores Clave:*
    *   **Frecuencia:** ¿Pulso mensual (check-in rápido) o Anual (profunda)?
    *   **Anonimato:** Crucial para temas sensibles.
    *   **Actionability:** "Si la respuesta es negativa, ¿puedo hacer algo al respecto?". Si no, no preguntes.
*   *Prompt de Diseño:*
    ```text
    Actúa como un Experto en People Analytics. 
    Diseña una estructura de encuesta de clima para [Empresa de Tecnología de 100 empleados en crecimiento rápido].
    
    OBJETIVO: Medir el impacto del reciente regreso a la oficina (RTO) y el burnout.
    RESTRICCIÓN: Máximo 10 preguntas.
    
    ESTRUCTURA REQUERIDA:
    1. 2 Preguntas de eNPS (Quantitative).
    2. 3 Preguntas sobre Work-Life Balance (Escala Likert 1-5).
    3. 2 Preguntas abiertas (Qualitative) diseñadas para obtener historias, no monosílabos.
    4. Justifica por qué elegiste cada pregunta abierta (qué sesgo evitas).
    ```

**Slide 8: Paso 2 - Auditoría de la Herramienta (Validación)**
*   *Acción:* Antes de lanzar, usa la IA como "Abogado del Diablo".
*   *Prompt de Auditoría:*
    ```text
    Critica estas preguntas que generaste. 
    1. ¿Alguna pregunta induce a una respuesta positiva (Leading Question)?
    2. ¿Son culturalmente sensibles para un equipo diverso?
    3. Reescribe las 2 más débiles para que sean más neutras y seguras psicológicamente.
    ```

**Slide 9: Paso 3 - El "Data Scientist" de Bolsillo (Análisis de CSV)**
*   *Contexto:* Tienes un Excel/CSV con 500 filas de comentarios abiertos sobre "¿Qué mejorarías de la empresa?".
*   *Prompt Maestro (Data Analysis):*
    ```text
    Actúa como un Senior People Analyst. 
    Analiza los comentarios del archivo adjunto (CSV).
    
    TAREA 1: SENTIMENT ANALYSIS
    - Clasifica el sentimiento general en: Positivo / Neutro / Negativo.
    - Dame el % aproximado de cada uno.

    TAREA 2: TOPIC MODELING
    - Identifica los 3 "Dolores Principales" (Pain Points) que más se repiten.
    - Para cada dolor, dame: 
      a) Una etiqueta clara (ej. "Burocracia Interna").
      b) La frecuencia estimada (Alta/Media/Baja).
      c) Dos citas textuales anónimas que representen mejor el problema.

    TAREA 3: RIESGO DE FUGA
    - Detecta señales sutiles de "intención de renuncia" o "burnout extremo". Cita ejemplos sin nombres.
    ```

**Slide 10: Paso 4 - Del Queja a la Solución (Action Plan)**
*   *Acción:* Convertir el reporte en iniciativas.
*   *Prompt de Ideación:*
    ```text
    Basado en el "Dolor Principal #1" identificado (ej. Falta de crecimiento profesional):
    Actúa como un Consultor de Liderazgo. 
    Proponme 3 iniciativas de bajo costo pero alto impacto (Quick Wins) para abordar esto en el próximo trimestre.
    Evita soluciones genéricas como "dar un curso". Sé creativo y accionable.
    ```

---

### Bloque 4: Hands-on / Workshop (45 min)
**Slide 11: Challenge - "El CEO está Furioso"**
*   *Escenario:* La encuesta de pulso acaba de salir y el eNPS cayó 20 puntos. El CEO quiere respuestas en 1 hora.
*   *Actividad:*
    1.  Toma el dataset de muestra (o tus datos propios anonimizados).
    2.  Ejecuta el **Prompt Maestro de Análisis**.
    3.  Genera el "Executive Summary".

**Slide 12: Redactando el Executive Summary**
*   *Prompt Sugerido:*
    ```text
    Usa el análisis anterior para escribir un correo al CEO.
    ESTRUCTURA:
    1. El Titular: La verdad en una frase (Bluf: Bottom Line Up Front).
    2. Los Datos: Los 3 drivers de la caída del eNPS.
    3. La Recomendación: Qué sugerimos hacer YA para detener la hemorragia.
    TONO: Directo, basado en datos, sin excusas, estratégico.
    ```

**Slide 13: Simulador de Crisis de Comunicación**
*   *Actividad:* "La gente está hablando en los pasillos sobre los despidos recientes".
*   *Prompt:*
    ```text
    Ayúdame a redactar el script para el All-Hands meeting de mañana. 
    La encuesta muestra miedo e incertidumbre. 
    Necesito un discurso que reconozca el dolor (empatía) pero que re-enfoque al equipo en el futuro (visión), sin prometer cosas que no podemos cumplir.
    ```

---

### Bloque 5: Cierre del Curso (15 min)
**Slide 14: El Viaje Completo (Recap S1-S5)**
*   *Visual:* Un mapa que conecta:
    *   S1: Productividad Personal (Tú).
    *   S2: Job Descriptions (Definir).
    *   S3: Entrevistas (Elegir).
    *   S4: Performance (Mejorar).
    *   S5: Cultura (Escuchar).

**Slide 15: Manifiesto HR + AI**
*   *Mensaje:* "La IA no reemplaza lo humano. La IA automatiza lo burocrático para que podamos ser *más* humanos."

**Slide 16: Compromiso de Acción**
*   *Actividad:* "Escribe en el chat: Una cosa que dejarás de hacer manualmente a partir del lunes."

**Slide 17: Despedida**
*   *Texto Final:* "Gracias por ser pioneros. El futuro del trabajo es de ustedes!"

