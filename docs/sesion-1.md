# Sesión 1: Fundamentos de IA para HR

## Bloque 1: Introducción y Contexto (30 min)

### Bienvenidos al Futuro (Ya llegó)
*   *Gancho:* "La IA no va a reemplazar a los profesionales de HR, pero los profesionales de HR que usan IA reemplazarán a los que no la usan".
*   *Objetivo:* Bajar la ansiedad y subir la curiosidad.

### ¿Qué es un LLM? (Explicado para humanos)
*   *Metáfora:* Es como un becario infinitamente leído pero sin sentido común propio.
*   *Concepto Clave:* Predicción de la siguiente palabra (Tokenization). No "piensa", calcula probabilidades basadas en patrones masivos de datos.
*   *Limitación:* Alucinaciones (cuando la probabilidad falla pero suena convincente).

### El Paisaje Actual (Modelos y Herramientas)
*   *Big 3:*
    *   **OpenAI (ChatGPT/o1):** El estándar de la industria.
    *   **Anthropic (Claude):** El más "humano" y seguro. Favorito para redacción y análisis complejo.
    *   **Google (Gemini):** Integración total con Google Workspace.
*   *Herramientas de Productividad:* Cursor (para código/docs), v0 (para interfaces), Perplexity (para búsqueda real).

---

## Bloque 2: Prompt Engineering - El Arte de Hablar con Máquinas (45 min)

### ¿Por qué importa el Prompting?
*   *Concepto:* "Garbage In, Garbage Out" (Basura entra, basura sale).
*   *Realidad:* La calidad de la respuesta depende 100% de la calidad de la instrucción.

### Caso de Éxito: Mercor (La IA que contrata)
*   *¿Qué hacen?:* Mercor es una startup valorada en miles de millones que conecta a expertos de dominio (médicos, abogados, programadores, financieros) con los laboratorios de IA más grandes (como OpenAI, Anthropic, Google).
*   *¿Cómo lo hacen?:* Su modelo de negocio se basa en el **RLHF (Reinforcement Learning from Human Feedback)**.
    1.  Reclutan a miles de profesionales altamente cualificados.
    2.  Estos expertos interactúan con los modelos, calificando respuestas y creando ejemplos perfectos ("Golden Data").
    3.  Si un modelo médico alucina un diagnóstico, un doctor real lo corrige. El modelo aprende de esa corrección experta.
*   *Lección:* Incluso las IAs más avanzadas del mundo dependen críticamente del criterio humano experto para mejorar y no alucinar. No es solo "datos", es "conocimiento humano estructurado".

### Anatomía del Prompt (C.R.I.F.) & Estructura Técnica
*   *Framework C.R.I.F.:* Fórmula para mejores resultados.
    *   **C**ontexto: Antecedentes necesarios.
    *   **R**ol: Persona que debe adoptar la IA.
    *   **I**nstrucción: Tarea específica.
    *   **F**ormato: Cómo quieres la entrega.
*   *Ejemplo Práctico:*
    *   *Contexto:* "Somos una empresa de software B2B lanzando un nuevo producto de nómina para PyMEs."
    *   *Rol:* "Actúa como un Gerente de Marketing Senior con experiencia en SaaS."
    *   *Instrucción:* "Escribe 3 correos de venta en frío (cold emails)."
    *   *Formato:* "Usa Markdown, tono profesional pero cercano, máximo 150 palabras por correo."
*   **Formatos Técnicos Potenciadores:**
    *   **XML Tags (`<tag>...</tag>`):**
        *   *¿Qué son?:* Etiquetas prestadas del lenguaje de marcado (como HTML) para separar claramente las secciones del prompt.
        *   *Beneficio:* Ayudan al modelo a distinguir dónde empiezan y terminan las instrucciones vs. los datos. Evita confusión.
        *   *Uso:* `<contexto>...</contexto>`, `<ejemplos>...</ejemplos>`, `<instrucción>...</instrucción>`.
    *   **Markdown (`.md`):**
        *   *¿Qué es?:* Un lenguaje de formato de texto ligero que usa símbolos simples (como # para títulos, * para listas).
        *   *Por qué usarlo:* Es el lenguaje nativo de los LLMs. Estructurar tu prompt con títulos y viñetas (bullets) mejora drásticamente la comprensión del modelo comparado con un bloque de texto plano.

::: tip 🚀 Demo Interactiva: Formatos de Prompts
¿Quieres ver la diferencia real entre Texto Plano, Markdown, HTML y XML?
[Explora la Demo en Vivo](https://v0-text-format-demo.vercel.app/)
:::

---

## Bloque 3: Live Demo (45 min)

### De lo Vago a lo Preciso
*   *Acción:* Mostrar ChatGPT en pantalla gigante.
*   *Prompt Malo:* "Dame ideas para un viaje". (Mostrar resultado genérico).
*   *Prompt Bueno (CRIF):* "Actúa como una agencia de viajes de lujo. Planea un viaje de 7 días a Italia para una familia con 2 niños (6 y 10 años), evitando museos aburridos y priorizando actividades al aire libre. Presupuesto medio. Formato: Tabla día por día."

### Caso de Uso Pro - Evaluación de Desempeño (HR Focus)
*   *Concepto:* Cómo usar la IA para sintetizar múltiples fuentes de datos (Feedback de pares, autoevaluación, notas del manager) en un documento coherente y profesional.
*   *Estructura del Prompt (Uso de XML Tags):*
```markdown
Actúa como un Manager de Operaciones Senior. Ayúdame a redactar la revisión de fin de año para un miembro de mi equipo llamada Elena. 
Tu objetivo es crear un resumen ejecutivo profesional y constructivo basado en las siguientes piezas de información:

<formato_de_salida>
1. Mirando Atrás: Logros clave del 2025 y áreas de desafío. 2-3 ejemplos de cómo aplicó nuestros principios operativos.
2. Mirando Adelante: Dos nuevos comportamientos o habilidades en los que Elena debe enfocarse para elevar su impacto.
</formato_de_salida>

<principios_operativos>
- El Cliente es el Norte: Trabajamos desde las necesidades del usuario.
- Excelencia en la Ejecución: Cuidamos el detalle y la calidad técnica.
- Colaboración sin Silos: Trabajamos como un solo equipo, sin egos.
- Mentalidad de Aprendizaje: Buscamos siempre aprender algo nuevo.
</principios_operativos>

<feedback_de_pares>
- Fortaleza: Entrega trabajo de alta calidad y es muy proactiva.
- Oportunidad: Podría delegar más y evitar sobrecargarse de tareas operativas.
</feedback_de_pares>

<autoevaluacion_de_elena>
- Destaca su éxito liderando la transición al Proyecto "Retail Flow".
- Obtuvo una certificación técnica en "Sistemas de Tesorería".
- Quiere enfocarse en mentoría el próximo año.
</autoevaluacion_de_elena>

<notas_del_manager_confidencial>
Elena tiene mucha energía pero a veces propone ideas que no están alineadas con la estrategia actual. 
Necesita primero sumergirse más en la nueva operación antes de intentar cambiarla. 
A veces se toma el feedback de forma personal; necesita madurez para entender que no es un ataque. 
Le asignaré liderar las "Calibraciones de Calidad" para que entienda los fundamentos antes de proponer cambios profundos.
</notas_del_manager_confidencial>

Prioriza mis notas (Manager) y busca patrones repetidos en el feedback de pares. Tono: Profesional, empático pero directo.
```

### Iteración en Vivo
*   *Acción:* Refinar el resultado anterior en vivo. "El tono suena muy duro en la parte de las ideas, suavízalo pero mantén la firmeza en que debe aprender primero la operación".


---

## Bloque 4: Hands-on / Workshop (45 min)

### Del Gimnasio al Laboratorio (HR Focus)
*   *Instrucción:* Ahora que entendemos la teoría, vamos a aplicarla en retos reales de HR comparando la "vieja forma" vs. la "nueva forma" de hablar con la IA.

### Reto 1 - El Salto de Calidad (Feedback Review)
*   *Objetivo:* Ver la diferencia entre un prompt genérico y uno específico (CRIF + XML).
*   *Paso 1 (La vieja forma):* Pide a la IA: "Escribe una evaluación de desempeño para Elena que trabajó bien pero debe mejorar su comunicación". 
    *   *Analiza:* ¿Qué tan genérico es el resultado?
*   *Paso 2 (La nueva forma):* Usa el framework del Bloque 3 (Slide 12). Pasa el contexto completo, separa con etiquetas `<contexto>`, `<feedback_manager>` y define un `<formato_salida>`.
    *   *Analiza:* ¿Cómo cambia la profundidad y utilidad del consejo?

### Reto 2 - Role-play: Manejo de Conversaciones Difíciles
*   *Objetivo:* Usar la IA como simulador para preparar una reunión real.
*   *Prompt Maestro:*
```text
Actúa como un empleado con alto potencial pero que recientemente ha bajado su 
rendimiento y se muestra defensivo. Yo seré tu manager. Empieza tú la 
conversación quejándote de que tienes demasiada carga de trabajo. Mi objetivo 
es entender la causa raíz y acordar un plan de mejora.
```
*   *Iteración Dinámica:* Después de un par de intercambios, dile a la IA:
```text
PAUSA. Sal del personaje. Actúa como mi Coach de HR y analiza mi última 
respuesta: ¿Fui empático? ¿Hice preguntas abiertas? ¿Cómo puedo mejorar mi enfoque?
```

### Reto 3 - El Filtro de Sesgos (Audit Mode)
*   *Objetivo:* Usar la IA para auditar nuestro propio juicio.
*   *Actividad:* Toma un párrafo de feedback que hayas escrito recientemente (o inventa uno).
*   *Prompt:* "Analiza este texto de feedback. ¿Hay sesgos inconscientes (de género, edad, cultura)? ¿El lenguaje es constructivo o punitivo? Dame 3 opciones para reescribirlo manteniendo el mensaje pero eliminando el sesgo."

---

## Bloque 5: Cierre (15 min)

### Share & Learn
*   *Dinámica:* 2-3 voluntarios comparten su "Wow moment" o su "Fail".
