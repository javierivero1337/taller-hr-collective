# Guía de Slides: Sesión 1
## Título: AI Literacy & Prompting Gym

**Objetivo:** Entender el "Roadmap", la filosofía "Human in the Loop" y perder el miedo mediante el Prompting básico.

---

### Bloque 1: Apertura (15 min)
**Slide 1: Portada**
*   *Texto:* LEADING HR IN THE AGE OF AI - Sesión 1: Alfabetización Digital.
*   *Visual:* Imagen impactante de humano + máquina colaborando.

**Slide 2: El Viaje (Roadmap)**
*   *Visual:* Línea de tiempo con las 5 sesiones (Diseño -> Selección -> Evaluación -> Clima).
*   *Key Point:* "Hoy construimos los cimientos. En las próximas semanas transformaremos todo el ciclo de talento."

**Slide 3: Icebreaker**
*   *Actividad:* "¿Cuál es tu mayor miedo con la IA?" (Lluvia de ideas en pizarra/post-its).
*   *Pregunta:* "¿Qué tan cómodos se sienten usando IA?" (Escala 1-5 o mano alzada).
*   *Discusión:* "¿Cómo usas la IA hoy en día?"

---

### Bloque 2: Teoría - Fundamentos y Paisaje Técnico (40 min)
**Slide 4: ¿Qué es un LLM? (El Cerebro)**
*   *Definición:* Large Language Model (Gran Modelo de Lenguaje). Motores de predicción de texto entrenados con gran parte de internet.
*   *Cómo funciona:* "Next Token Prediction". No razona como un humano, calcula probabilísticamente cuál es la siguiente palabra más lógica.
*   *Metáfora:* La "Biblioteca Predictiva". Imagina a alguien que ha leído todos los libros pero nunca ha salido a la calle. Sabe mucho, pero todo es teórico y basado en patrones.

**Slide 5: ¿Qué es un Agente? (Cerebro + Manos)**
*   *Evolución:* El LLM es pasivo (espera tu prompt). El Agente es activo (tiene objetivos y usa herramientas).
*   *Diferencia Clave:*
    *   *LLM:* Le pides una receta.
    *   *Agente:* Le pides que compre los ingredientes en el súper online y te los envíe a casa.
*   *En HR:* Un LLM redacta un contrato. Un Agente redacta el contrato, lo envía a firma digital y notifica a nómina cuando está firmado.
*   Ejemplo: Agentic Commerce dentro de ChatGPT con Stripe

**Slide 6: El Paisaje de Modelos (Tu Equipo de Trabajo - Edición 2025/2026)**
*   **OpenAI (El Estándar de Razonamiento):**
    *   *Modelos Clave:* **GPT-5.2** (Thinking, Pro, Instant) y GPT-5.
    *   *Rol:* El "Científico". Especializado en problemas abiertos, matemáticas y teoría de aprendizaje. Sus modos "Thinking" permiten razonamiento largo antes de responder.
*   **Google DeepMind (Inteligencia Multimodal):**
    *   *Modelos Clave:* **Gemini 3** (Deep Think, Pro, Flash).
    *   *Rol:* El "Analista Total". Multimodal nativo (procesa video, audio y texto fluidamente). Gemini 3 representa una nueva era de capacidad cognitiva.
*   **Anthropic (Seguridad y Matiz Humano):**
    *   *Modelos Clave:* **Claude 4.5 Opus** y Claude 4.
    *   *Rol:* El "Estratega Seguro". Optimizado para tareas complejas y redacción matizada. Foco en seguridad empresarial y alineación ética.
*   **Open Source & Otros (La Revolución Abierta):**
    *   *Meta (Llama 4):* Inteligencia multimodal nativa y abierta.
    *   *DeepSeek (V3.2-Exp):* Eficiencia extrema con "Sparse Attention" y modos de pensamiento.
    *   *Zhipu AI (GLM-4.6):* Potente en agencia (acciones autónomas) y codificación.

**Slide 7: Velocidad vs. Inteligencia (Cost Management)**
*   *Concepto:* No contratas a un PhD para servir café. Eficiencia de recursos.
*   *Modelos "Flash/Mini":* Rápidos, baratos. Para tareas simples y repetitivas.
*   *Modelos "Pro/Sonnet/Opus":* Potentes, caros. Para razonamiento complejo y estrategia.

**Slide 8: Conceptos Técnicos Clave**
*   **Token (La Unidad de Procesamiento):**
    *   *Concepto:* Los LLMs no leen palabras completas, leen fragmentos de caracteres.
    *   *Regla:* 1,000 tokens ≈ 750 palabras.
    *   *Tipos:*
        *   **Input Tokens (Entrada):** Lo que tú le escribes o envías (tu prompt + documentos adjuntos). Suelen ser más baratos y rápidos de procesar.
        *   **Output Tokens (Salida):** Lo que la IA genera respuesta. Suelen ser más costosos y lentos, ya que requieren más capacidad de cómputo para "pensar" cada palabra.
    *   *Ejemplo:* La palabra "Hamburguesa" puede ser 1 token, pero "Antiinconstitucionalmente" serán varios. Es la moneda de cambio.
*   **Context Window (La Memoria de Trabajo):**
    *   *Concepto:* Es la cantidad de información que el modelo puede "mantener en su cabeza" simultáneamente durante una conversación.
    *   *Analogía:* Es como la superficie de un escritorio. Si tienes un escritorio pequeño (ventana corta), solo caben un par de hojas. Si es enorme (ventana larga, como Gemini 1.5), caben libros enteros.
    *   *Importancia:* Si excedes la ventana, el modelo "olvida" el inicio de la conversación.
*   **Temperatura (Creatividad vs. Precisión):**
    *   *Concepto:* Parámetro que controla la aleatoriedad de la respuesta (Escala 0.0 a 1.0).
    *   *Uso:*
        *   *Temp 0 (Baja):* Respuestas deterministas, lógicas y precisas. Ideal para código, matemáticas o extracción de datos.
        *   *Temp 0.8+ (Alta):* Respuestas variadas, creativas y menos predecibles. Ideal para lluvia de ideas o escritura creativa.

**Slide 9: Human in the Loop (HITL) & Alucinaciones**
*   *Riesgo:* Las "Alucinaciones" son errores presentados con confianza.
*   *Filosofía:* La IA es el copiloto. El humano siempre define el objetivo, supervisa y valida.
*   *Diagrama:* Humano (Contexto) -> IA (Borrador) -> Humano (Edición/Juicio).
*   **Business Case: Mercor (La industrialización del HITL)**
    *   *¿Qué hacen?:* Mercor es una startup valorada en miles de millones que conecta a expertos de dominio (médicos, abogados, programadores, financieros) con los laboratorios de IA más grandes (como OpenAI, Anthropic, Google).
    *   *¿Cómo lo hacen?:* Su modelo de negocio se basa en el **RLHF (Reinforcement Learning from Human Feedback)**.
        1.  Reclutan a miles de profesionales altamente cualificados.
        2.  Estos expertos interactúan con los modelos, calificando respuestas y creando ejemplos perfectos ("Golden Data").
        3.  Si un modelo médico alucina un diagnóstico, un doctor real lo corrige. El modelo aprende de esa corrección experta.
    *   *Lección:* Incluso las IAs más avanzadas del mundo dependen críticamente del criterio humano experto para mejorar y no alucinar. No es solo "datos", es "conocimiento humano estructurado".

**Slide 10: Anatomía del Prompt (C.R.I.F.) & Estructura Técnica**
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

---

### Bloque 3: Live Demo (45 min)
**Slide 11: De lo Vago a lo Preciso**
*   *Acción:* Mostrar ChatGPT en pantalla gigante.
*   *Prompt Malo:* "Dame ideas para un viaje". (Mostrar resultado genérico).
*   *Prompt Bueno (CRIF):* "Actúa como una agencia de viajes de lujo. Planea un viaje de 7 días a Italia para una familia con 2 niños (6 y 10 años), evitando museos aburridos y priorizando actividades al aire libre. Presupuesto medio. Formato: Tabla día por día."

**Slide 12: Caso de Uso Pro - Evaluación de Desempeño (HR Focus)**
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

**Slide 13: Iteración en Vivo**
*   *Acción:* Refinar el resultado anterior en vivo. "El tono suena muy duro en la parte de las ideas, suavízalo pero mantén la firmeza en que debe aprender primero la operación".


---

### Bloque 4: Hands-on / Workshop (45 min)
**Slide 14: Del Gimnasio al Laboratorio (HR Focus)**
*   *Instrucción:* Ahora que entendemos la teoría, vamos a aplicarla en retos reales de HR comparando la "vieja forma" vs. la "nueva forma" de hablar con la IA.

**Slide 15: Reto 1 - El Salto de Calidad (Feedback Review)**
*   *Objetivo:* Ver la diferencia entre un prompt genérico y uno específico (CRIF + XML).
*   *Paso 1 (La vieja forma):* Pide a la IA: "Escribe una evaluación de desempeño para Elena que trabajó bien pero debe mejorar su comunicación". 
    *   *Analiza:* ¿Qué tan genérico es el resultado?
*   *Paso 2 (La nueva forma):* Usa el framework del Bloque 3 (Slide 12). Pasa el contexto completo, separa con etiquetas `<contexto>`, `<feedback_manager>` y define un `<formato_salida>`.
    *   *Analiza:* ¿Cómo cambia la profundidad y utilidad del consejo?

**Slide 16: Reto 2 - Role-play: Manejo de Conversaciones Difíciles**
*   *Objetivo:* Usar la IA como simulador para preparar una reunión real.
*   *Prompt Maestro:* "Actúa como un empleado con alto potencial pero que recientemente ha bajado su rendimiento y se muestra defensivo. Yo seré tu manager. Empieza tú la conversación quejándote de que tienes demasiada carga de trabajo. Mi objetivo es entender la causa raíz y acordar un plan de mejora."
*   *Iteración Dinámica:* Después de un par de intercambios, dile a la IA: "PAUSA. Sal del personaje. Actúa como mi Coach de HR y analiza mi última respuesta: ¿Fui empático? ¿Hice preguntas abiertas? ¿Cómo puedo mejorar mi enfoque?"

**Slide 17: Reto 3 - El Filtro de Sesgos (Audit Mode)**
*   *Objetivo:* Usar la IA para auditar nuestro propio juicio.
*   *Actividad:* Toma un párrafo de feedback que hayas escrito recientemente (o inventa uno).
*   *Prompt:* "Analiza este texto de feedback. ¿Hay sesgos inconscientes (de género, edad, cultura)? ¿El lenguaje es constructivo o punitivo? Dame 3 opciones para reescribirlo manteniendo el mensaje pero eliminando el sesgo."

---

### Bloque 5: Cierre (15 min)
**Slide 18: Share & Learn**
*   *Dinámica:* 2-3 voluntarios comparten su "Wow moment" o su "Fail".
