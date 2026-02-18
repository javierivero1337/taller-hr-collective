# Sesión 5: Voice of the Employee 

## Bloque 1: Apertura (15 min)

### La Brecha del Compromiso (The Engagement Gap)
*   *Dato:* "El 80% de las empresas mide el engagement, pero solo el 20% toma acciones que los empleados perciben."
*   *El Problema:* Las encuestas anuales son autopsias. Llegan tarde.
*   *El Dolor:* Tenemos 1,000 comentarios abiertos. Leerlos toma semanas. Entenderlos toma meses. Accionar toma años.

### El "Agujero Negro" de la Data Cualitativa
*   *Situación:* RRHH ama los gráficos (Quantitative), pero ignora los comentarios de texto (Qualitative) por falta de tiempo.
*   *Riesgo:* En el texto libre es donde están las señales tempranas de renuncia (Burnout, Toxicidad, Acoso).
*   *Solución:* Usar IA para "escuchar" a escala masiva en segundos, no semanas.

## Bloque 2: Teoría (30 min)

### Más allá del Word Cloud (Nube de Palabras)
*   *Crítica:* Las nubes de palabras no sirven. Que la palabra "Salario" sea grande no nos dice si la gente está feliz o furiosa con él.
*   *Concepto 1: Análisis de Sentimiento*: La IA clasifica la "temperatura" emocional de un texto (Positivo, Negativo, Neutro, Mixto).
    *   **Teoría:** No solo busca palabras clave, sino que analiza el contexto (semántica). Detecta sarcasmo, intensidad y matices.
    *   **Ejemplo:** 
        *   *"El nuevo proceso de evaluación es... interesante"* → La IA puede detectar un sentimiento **Negativo/Sarcástico** a pesar de usar una palabra neutra.
        *   *"Me encanta el equipo, pero el proceso de aprobación es un infierno"* → Sentimiento **Mixto** (Positivo para cultura, Negativo para procesos).
    *   **Caso Real:** Una empresa de retail detectó una caída en el sentimiento positivo un mes *antes* de una ola de renuncias masivas, permitiendo a RRHH intervenir en las tiendas más críticas.
    *   **Visualización (Reporte Mock):**
        | Área / Categoría | Sentimiento | Confianza | Resumen de Comentarios |
        | :--- | :---: | :---: | :--- |
        | **Liderazgo (Management)** | 🟡 Mixto | 92% | Alta valoración de la cercanía de los managers, pero críticas por falta de claridad en objetivos estratégicos. |
        | **Cultura y Bienestar** | 🟢 Positivo | 98% | Fuerte sentido de pertenencia y apoyo entre compañeros. El trabajo híbrido es el beneficio mejor valorado. |
        | **Compensación y Beneficios** | 🔴 Negativo | 95% | Descontento general con la falta de transparencia en las bandas salariales y la actualización por inflación. |
        | **Herramientas y Procesos** | 🟡 Mixto | 89% | Se aprecia la autonomía, pero hay frustración por la burocracia en procesos de aprobación simples. |

*   *Concepto 2: Topic Modeling (Modelado de Temas)*: La IA agrupa comentarios dispares bajo etiquetas inteligentes (ej. "Balance Vida-Trabajo", "Liderazgo Directivo", "Herramientas de Trabajo").
    *   **Teoría:** Utiliza algoritmos para encontrar patrones ocultos. No necesita que tú le digas qué buscar; la IA "descubre" de qué está hablando la gente.
    *   **Ejemplo:** De 500 comentarios, la IA identifica que el 40% habla de "Fricción Tecnológica" (VPN lenta, software antiguo) y el 20% de "Microgestión".
    *   **Caso Real:** Una startup tecnológica creía que su problema era el "Salario". Al aplicar Topic Modeling, descubrieron que el tema real era "Herramientas de Trabajo": los desarrolladores estaban frustrados por usar laptops obsoletas, no por su sueldo. Cambiar las laptops costó menos que subir sueldos y resolvió el clima.
    *   **Visualización (Reporte Mock):**
        | Tema Identificado | Frecuencia | Sentimiento Promedio | Acción Recomendada |
        | :--- | :---: | :---: | :--- |
        | **Fricción Tecnológica** | 42% | 🔴 Negativo | Auditoría de hardware y VPN. |
        | **Cultura de Equipo** | 35% | 🟢 Positivo | Reforzar programas de reconocimiento. |
        | **Claridad de Objetivos** | 23% | 🟡 Neutro | Revisar metodología OKR con managers. |

### Privacidad y Ética (El "Must-Have")
*   *Regla de Oro:* **Zero PII (Personally Identifiable Information)**.
*   *Protocolo de Seguridad:*
    1.  Eliminar columnas de Nombres, Emails, IDs.
    2.  Buscar/Reemplazar nombres de jefes específicos en los comentarios.
    3.  Opt-out de usar datos para entrenamiento (Configuración de privacidad en ChatGPT Team/Enterprise).

### La Pirámide de la Acción
*   *Base:* Datos Crudos (Encuestas).
*   *Medio:* Insights (Lo que la IA nos dice).
*   *Cima:* Decisiones (Lo que RRHH hace).
*   La IA nos lleva de la Base al Medio instantáneamente para que nosotros pasemos el 100% del tiempo en la Cima.

## Bloque 3: Live Demo (45 min)

### Paso 1 - Diseñando la Encuesta Perfecta (Pre-Medición)
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

### Paso 2 - Auditoría de la Herramienta (Fricción y Calidad)
*   *Acción:* Antes de lanzar, usa la IA como "Abogado del Diablo" para asegurar que los datos que recojas sean útiles y no ruido.
*   *Prompt de Auditoría de Calidad:*
    ```text
    Actúa como un experto en Psicometría y Diseño de Encuestas. 
    Analiza las preguntas que generamos anteriormente para asegurar que los datos resultantes sean de alta calidad.
    
    CRITERIOS DE AUDITORÍA:
    1. Fatiga del Encuestado: ¿Hay preguntas redundantes que podamos eliminar para aumentar la tasa de completitud?
    2. Sesgo de Respuesta: ¿Alguna pregunta está redactada de forma que empuja al empleado a responder positivamente (Leading Question)?
    3. Ambigüedad: ¿Hay términos vagos que diferentes personas podrían interpretar de distintas maneras?
    4. Accionabilidad: Si una pregunta sale con puntaje bajo, ¿el resultado nos da una pista clara de qué acción tomar o es demasiado genérica?
    
    Reescribe las preguntas necesarias para que sean directas, neutras y diseñadas para obtener insights accionables.
    ```

### Paso 3 - El "Data Scientist" de Bolsillo (Análisis de CSV)
*   *Contexto:* Tienes un Excel/CSV con 500 filas de comentarios abiertos sobre "¿Qué mejorarías de la empresa?".
*   *Prompt Maestro (Data Analysis):*
    ```text
    Actúa como un Senior People Analyst experto en NLP (Natural Language Processing). 
    Analiza los comentarios del archivo adjunto (CSV) siguiendo esta estructura rigurosa:
    
    TAREA 1: SENTIMENT ANALYSIS (Visión Estratégica)
    - Genera un reporte por Áreas/Categorías (ej. Liderazgo, Cultura, Compensación, Procesos).
    - Para cada área, indica: Sentimiento (Positivo/Neutro/Negativo/Mixto), % de Confianza de la IA y un resumen ejecutivo de los comentarios que justifique esa clasificación.
    
    TAREA 2: TOPIC MODELING (Descubrimiento de Patrones)
    - Identifica los temas emergentes sin usar categorías predefinidas.
    - Para cada tema, genera una tabla con:
      a) Tema Identificado (ej. "Fricción Tecnológica").
      b) Frecuencia (% de menciones sobre el total).
      c) Sentimiento Promedio del tema.
      d) Acción Recomendada específica para RRHH.
    
    TAREA 3: RIESGOS CRÍTICOS Y "EARLY WARNINGS"
    - Detecta señales de Burnout, intención de renuncia o toxicidad.
    - Cita 2 ejemplos textuales (anonimizados) representativos de cada riesgo.
    
    FORMATO DE SALIDA: Usa tablas markdown para las visualizaciones de sentimiento y temas, tal como un reporte ejecutivo de People Analytics.
    ```

::: tip 📥 Recurso para Práctica
[**Descargar Dataset de Ejemplo (Mock Responses)**](./mock-responses.md)  
Este archivo contiene 250 respuestas simuladas de una startup en crecimiento. Úsalo para copiar y pegar en la IA y probar el prompt anterior.
:::


## Bloque 4: Hands-on / Workshop (45 min)

### Challenge - "El CEO está Furioso"
*   *Escenario:* La encuesta de pulso acaba de salir y el eNPS cayó 20 puntos. El CEO quiere respuestas en 1 hora.
*   *Actividad:*
    1.  Toma el dataset de muestra (o tus datos propios anonimizados).
    2.  Ejecuta el **Prompt Maestro de Análisis**.
    3.  Genera el "Executive Summary".

### Redactando el Executive Summary
*   *Prompt Sugerido:*
    ```text
    Usa el análisis anterior para escribir un correo al CEO.
    ESTRUCTURA:
    1. El Titular: La verdad en una frase (Bluf: Bottom Line Up Front).
    2. Los Datos: Los 3 drivers de la caída del eNPS.
    3. La Recomendación: Qué sugerimos hacer YA para detener la hemorragia.
    TONO: Directo, basado en datos, sin excusas, estratégico.
    ```

### Simulador de Crisis de Comunicación
*   *Actividad:* "La gente está hablando en los pasillos sobre los despidos recientes".
*   *Prompt:*
    ```text
    Ayúdame a redactar el script para el All-Hands meeting de mañana. 
    La encuesta muestra miedo e incertidumbre. 
    Necesito un discurso que reconozca el dolor (empatía) pero que re-enfoque al equipo en el futuro (visión), sin prometer cosas que no podemos cumplir.
    ```

## Bloque 5: Cierre del Curso (15 min)

### El Viaje Completo (Recap S1-S5)

*   S1: Productividad Personal (Tú).
*   S2: Job Descriptions (Definir).
*   S3: Entrevistas (Elegir).
*   S4: Performance (Mejorar).
*   S5: Cultura (Escuchar).


<div style="margin: 2rem auto; max-width: 640px; padding: 2rem 2.5rem; border-left: 4px solid var(--vp-c-brand-1); background: var(--vp-c-brand-soft); border-radius: 0 12px 12px 0; text-align: center;">
  <p style="font-size: 1.35rem; font-weight: 600; line-height: 1.6; color: var(--vp-c-text-1); margin: 0; font-style: italic;">
    "La IA no reemplaza lo humano.<br>La IA automatiza lo burocrático<br>para que podamos ser <span style="color: var(--vp-c-brand-1); font-weight: 800;">más humanos</span>."
  </p>
</div>
