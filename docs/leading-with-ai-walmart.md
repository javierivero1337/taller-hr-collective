# Leading with AI – Walmart

## Ficha Técnica

| Concepto | Detalle |
| :--- | :--- |
| **Nombre de la sesión** | Leading with AI – Walmart |
| **Duración** | 4 horas |
| **Modalidad** | Presencial / Sincrónica |
| **Audiencia** | Líderes y equipos de distintas tribus con uso frecuente de herramientas de IA |
| **Nivel esperado** | Intermedio funcional: usuarios activos de IA que necesitan elevar su uso hacia pensamiento estratégico, análisis crítico y decisiones accionables |
| **Herramientas sugeridas** | Copilot, ChatGPT, Gemini, Excel, Power BI, documentos propios anonimizados |

### Propósito

Esta sesión busca mover a los participantes de un uso productivo pero aislado de IA hacia una forma más estratégica de liderar con IA: definir mejor problemas, formular mejores preguntas, analizar datos con hipótesis, cuestionar supuestos y construir planes de acción defendibles.

La promesa no es "hacer mejores prompts". La promesa es aprender a dirigir una investigación asistida por IA desde una situación ambigua hasta una decisión accionable.

### Resultado Esperado

Al final de la sesión, cada equipo habrá construido un **AI Decision Brief** basado en un caso real de su tribu, incluyendo:

- Problema definido con claridad.
- Set inicial de preguntas estratégicas para investigar los datos.
- Hipótesis priorizadas.
- Análisis asistido por IA con evidencia, límites y riesgos.
- Plan de acción de 30 días con métrica de éxito.

---

## Agenda General

| Bloque | Duración | Enfoque |
| :--- | :---: | :--- |
| 1. AI Literacy para líderes | 60 min | Tokens, LLMs, contexto, modelos y límites |
| 2. Del dato a la pregunta | 35 min | Diseñar preguntas estratégicas antes de analizar |
| 3. Definición del problema e hipótesis | 35 min | Separar síntomas, causas y decisiones |
| 4. Análisis asistido por IA | 45 min | Evaluar hipótesis con evidencia y límites |
| 5. Plan de acción y pitch ejecutivo | 65 min | Convertir hallazgos en decisión defendible |

---

## Bloque 1: AI Literacy Para Líderes (60 min)

### Objetivo

Dar una base conceptual común para que los participantes entiendan cómo funciona la IA generativa, por qué el contexto cambia la calidad del análisis y qué modelo conviene usar según el tipo de tarea.

Este bloque debe evitar una explicación técnica profunda. La meta es que los líderes entiendan cómo dirigir mejor a la IA.

### 1.1 Qué Es Un LLM (12 min)

Un LLM es un modelo entrenado para predecir la siguiente palabra o fragmento de texto con base en patrones aprendidos. No "sabe" en el sentido humano; genera respuestas plausibles a partir de contexto, entrenamiento e instrucciones.

Conceptos clave:

- **Predicción, no verdad:** una respuesta puede sonar convincente y estar equivocada.
- **Patrones, no criterio propio:** el criterio lo aporta el humano.
- **Lenguaje como interfaz:** la calidad de la instrucción cambia la calidad del pensamiento asistido.
- **Human in the loop:** la IA propone, el humano decide.

Pregunta para discusión:

> Si la IA puede sonar segura aunque esté equivocada, ¿en qué decisiones de tu tribu sería peligroso usarla sin revisión humana?

### 1.2 Tokens y Contexto (12 min)

Los modelos no leen como humanos. Procesan texto en unidades llamadas **tokens**. Todo lo que se escribe en la conversación ocupa espacio dentro de una ventana de contexto.

Ideas clave:

- Un token puede ser una palabra corta, parte de una palabra o signo de puntuación.
- La ventana de contexto es la "memoria de trabajo" del modelo durante una conversación.
- Si el contexto es pobre, la respuesta será genérica.
- Si el contexto está desordenado, la IA puede mezclar prioridades.
- Más contexto no siempre es mejor; mejor contexto sí.

Ejemplo rápido:

Prompt débil:

```text
Analiza estos datos y dame recomendaciones.
```

Prompt con contexto:

```text
Actúa como un líder de estrategia para retail.

Estoy analizando datos de [tipo de proceso] para decidir dónde intervenir primero.
Mi objetivo no es encontrar todos los patrones, sino identificar las 3 oportunidades con mayor impacto operativo en los próximos 30 días.

Antes de concluir, separa evidencia de interpretación y dime qué no podemos afirmar con estos datos.
```

Principio:

> La IA no mejora solo porque le damos más datos. Mejora cuando le damos objetivo, contexto, restricciones y criterios de calidad.

### 1.3 Habla Mejor Con Tu LLM (12 min)

Un LLM responde mejor cuando la información está estructurada. No hay que programar para hablar mejor con IA, pero sí ayuda usar formatos que separen instrucciones, contexto y datos.

Tres formatos útiles:

- **Markdown:** forma simple de estructurar texto con títulos, listas, tablas y bloques. Ayuda a que la IA distinga jerarquía e intención.
- **XML:** etiquetas como `<contexto>`, `<datos>` o `<instruccion>` que delimitan secciones. Sirve para evitar que la IA mezcle datos con órdenes.
- **CSV:** archivo o texto tabular separado por comas. Sirve para compartir datos estructurados de Excel, encuestas o reportes.

Ejemplo en Markdown:

```markdown
# Objetivo
Identificar los 3 riesgos principales en estos comentarios.

## Reglas
- No inventes causas.
- Separa evidencia de interpretación.
- Declara qué datos faltan.
```

Ejemplo con XML:

```xml
<contexto>
Estamos revisando comentarios abiertos de una encuesta de clima.
</contexto>

<instruccion>
Identifica patrones repetidos y riesgos accionables.
</instruccion>

<formato_salida>
Entrega una tabla con tema, evidencia, riesgo y acción sugerida.
</formato_salida>
```

Ejemplo CSV:

```csv
tribu,puntaje,comentario
People,3,"Hay buena colaboración, pero falta claridad de carrera"
Finanzas,2,"El proceso de cierre consume demasiado tiempo manual"
Supply,4,"La coordinación mejoró, aunque seguimos con retrabajo"
```

Regla práctica:

> Si el prompt parece un párrafo gigante, probablemente la IA tendrá que adivinar demasiado. Si el prompt tiene estructura, la IA puede razonar con más orden.

### 1.4 Modelos: Cuál Usar Para Qué (12 min)

No todos los modelos son iguales. Para liderar con IA, conviene pensar en el tipo de trabajo que necesitamos.

| Tipo de tarea | Qué necesitamos del modelo |
| :--- | :--- |
| Redacción ejecutiva | Claridad, tono, síntesis |
| Análisis de datos | Capacidad de interpretar estructuras, tablas y patrones |
| Investigación | Búsqueda, comparación de fuentes, trazabilidad |
| Planeación estratégica | Razonamiento, trade-offs, escenarios |
| Revisión crítica | Capacidad de detectar supuestos débiles y riesgos |
| Automatización | Consistencia, instrucciones repetibles, integración con herramientas |

Discusión:

> ¿En qué casos usarías la IA como redactor, analista, auditor, coach o comité ejecutivo escéptico?

### 1.5 Limitaciones: Alucinaciones, Sesgos y Falsa Certeza (12 min)

La IA puede fallar de formas que parecen inteligentes:

- Inventar datos o causas.
- Confundir correlación con causalidad.
- Sobreconcluir a partir de poca evidencia.
- Reforzar sesgos presentes en los datos.
- Proponer planes de acción que suenan bien pero no son operables.

Regla operativa:

> En decisiones de negocio, no pedir "la respuesta". Pedir evidencia, supuestos, límites, alternativas y riesgos.

Prompt de control:

```text
Antes de darme una recomendación, dime:
1. Qué evidencia sí soporta la conclusión.
2. Qué evidencia la contradice.
3. Qué supuestos estás haciendo.
4. Qué dato adicional cambiaría tu recomendación.
5. Qué decisión sería prematura tomar.
```

---

## Bloque 2: Del Dato A La Pregunta (35 min)

### Objetivo

Evitar que los participantes usen la IA para saltar demasiado rápido a conclusiones. El primer músculo avanzado es aprender a preguntar mejor antes de analizar.

### Selección Del Caso En Equipos De 3

Antes de usar IA, formen equipos de 3 y elijan un set de datos, reporte o documento de trabajo que esté conectado a un problema real. No sirve tomar un reporte simple solo porque existe; el caso debe tener una decisión pendiente, una tensión operativa o una oportunidad que valga la pena investigar.

El caso elegido debe cumplir con estas características:

- **Tiene un problema o decisión viva:** hay algo que el equipo necesita entender, priorizar o resolver.
- **Permite más de una explicación posible:** si la causa ya es obvia, el ejercicio pierde valor.
- **Tiene datos suficientes para preguntar:** incluye comentarios, métricas, segmentos, periodos, categorías, tickets, casos o evidencias comparables.
- **Puede llevar a una acción concreta:** idealmente permite proponer un experimento o decisión de 30 días.
- **Tiene contexto de negocio:** el equipo puede explicar qué significan las columnas, métricas, comentarios o documentos.
- **No depende de que la IA invente información:** los datos deben permitir analizar algo real, aunque sea de forma parcial.

Buenos ejemplos:

- Comentarios abiertos de encuestas de clima, cultura o experiencia donde hay preocupación por algún patrón.
- Reportes de ventas, merma, productividad, rotación o desempeño con variaciones que requieren explicación.
- Minutas, hallazgos, tickets, quejas, solicitudes o consultas recurrentes que podrían revelar fricciones operativas.
- Comparativos de proveedores, contratos, iniciativas o campañas donde hay una decisión por tomar.
- Bases de datos operativas con señales de retrabajo, cuellos de botella, tiempos altos o oportunidades de eficiencia.
- Presentaciones o documentos estratégicos que necesitan convertirse en preguntas, hipótesis y plan de acción.

Casos que no funcionan bien:

- Reportes puramente informativos sin problema o decisión asociada.
- Datos demasiado agregados donde no se puede comparar nada.
- Casos donde el equipo no entiende el origen o significado de los datos.
- Situaciones donde ya se decidió la acción y solo se busca justificarla.

### Dinámica

Cada equipo trabaja con el caso seleccionado y mantiene el mismo set de datos durante todo el ejercicio. La IA puede ayudar a formular preguntas, hipótesis y planes, pero el equipo debe aportar el criterio de negocio.

La instrucción principal:

> No vamos a analizar todavía. Primero vamos a descubrir qué preguntas vale la pena hacer.

### Prompt Maestro 1: Diseñador De Preguntas

```text
Actúa como un Chief Strategy Officer y analista senior de datos para Walmart.

Tengo este caso:

<contexto_del_caso>
[Describe extensamente el proceso, área, decisión o problema]
</contexto_del_caso>

<datos_disponibles>
[Describe lo más detallado tu archivo anexo, como si lo estuvieras explicando a una persona de nuevo ingreso y pega una muestra del dataset, comentarios, reporte o documentos]
</datos_disponibles>

No analices todavía ni des conclusiones.

Primero ayúdame a diseñar las mejores preguntas que deberíamos hacerle a estos datos para encontrar oportunidades, riesgos, patrones ocultos y posibles decisiones de negocio.

Clasifica las preguntas en:
1. Preguntas descriptivas: qué está pasando.
2. Preguntas diagnósticas: por qué podría estar pasando.
3. Preguntas predictivas: qué podría pasar si no actuamos.
4. Preguntas prescriptivas: qué decisiones podríamos tomar.
5. Preguntas incómodas: qué supuestos deberíamos cuestionar.

Para cada pregunta, explica:
- Por qué importa.
- Qué dato ayudaría a responderla.
- Qué decisión podría habilitar.
```

### Output Del Bloque

Cada equipo selecciona sus **3 preguntas más poderosas** y descarta las preguntas que sean interesantes pero no accionables.

Checklist de selección:

- ¿La pregunta puede cambiar una decisión?
- ¿La pregunta puede responderse parcialmente con los datos disponibles?
- ¿La pregunta evita asumir una causa antes de verla?
- ¿La pregunta conecta con impacto de negocio o experiencia de asociado/cliente?

---

## Bloque 3: Definición Del Problema E Hipótesis (35 min)

### Objetivo

Convertir una pregunta amplia en un problema claro, separando síntomas de causas posibles.

Ejemplo:

- Débil: "Queremos analizar rotación."
- Mejor: "Queremos entender si la rotación en ciertos equipos está relacionada con falta de claridad de carrera, carga operativa o liderazgo directo, para decidir dónde intervenir primero."

### Prompt Maestro 2: Definidor Del Problema

```text
Actúa como un consultor senior de estrategia y transformación organizacional.

Esta es la pregunta que queremos investigar:

<pregunta_prioritaria>
[Pegar pregunta seleccionada]
</pregunta_prioritaria>

Este es el contexto del negocio:

<contexto>
[Pegar contexto extensivo del equipo, tribu, proceso o decisión. Entre más detallado mejor]
</contexto>

Ayúdame a convertir esta pregunta en un problema bien definido.

Quiero que me ayudes a:
1. Separar síntomas de causas posibles.
2. Redactar el problema en una frase clara.
3. Identificar qué evidencia necesitaríamos para validarlo.
4. Señalar qué conclusiones NO podríamos sacar con los datos actuales.
5. Proponer 3 hipótesis investigables.
6. Priorizar las hipótesis según impacto potencial y factibilidad de análisis.

Formato:
- Problema definido.
- Síntomas observados.
- Causas posibles.
- Hipótesis priorizadas.
- Evidencia necesaria.
- Límites del análisis.
```

### Actividad

Cada equipo debe elegir **una hipótesis principal** y **una hipótesis alternativa**.

Esto fuerza pensamiento crítico: no basta con confirmar lo que ya creemos.

### Output Del Bloque

Un problema redactado en una frase:

```text
Queremos entender si [posible causa o patrón] está afectando [resultado observable] en [población/proceso], para decidir [acción o decisión concreta].
```

---

## Bloque 4: Análisis Asistido Por IA (45 min)

### Objetivo

Usar IA para analizar evidencia contra hipótesis, no para producir insights genéricos.

### Prompt Maestro 3: Analista De Hipótesis

```text
Actúa como un analista senior de estrategia, datos y operaciones.

Vamos a analizar los datos con base en hipótesis, no buscando conclusiones genéricas.

<problema_definido>
[Pegar problema definido]
</problema_definido>

<hipotesis>
1. [Hipótesis principal]
2. [Hipótesis alternativa]
</hipotesis>

<datos>
[Pegar el mismo set de datos del caso usado en los prompts anteriores.
Si el dataset es muy grande, pegar una muestra representativa y/o el resumen de hallazgos generado hasta ahora.]
</datos>

Para cada hipótesis, indica:
1. Evidencia que la apoya.
2. Evidencia que la contradice.
3. Patrones relevantes.
4. Nivel de confianza: alto, medio o bajo.
5. Qué dato adicional necesitaríamos.
6. Qué conclusión sería prematura.
7. Qué implicación tendría para la decisión.

Reglas:
- No inventes datos.
- Separa evidencia de interpretación.
- Si el dataset no permite responder algo, dilo explícitamente.
- No confundas correlación con causalidad.
```

### Actividad

Los equipos revisan el análisis y marcan cada hallazgo como:

- **Evidencia fuerte:** aparece en datos claros o patrones repetidos.
- **Evidencia débil:** podría ser útil, pero requiere más validación.
- **Interpretación:** explicación plausible, pero no comprobada.
- **Ruido:** interesante pero no accionable.

### Output Del Bloque

Un mini mapa de decisión:

```text
Hipótesis más probable:
Evidencia principal:
Nivel de confianza:
Dato que falta:
Decisión que sí podemos tomar:
Decisión que todavía no deberíamos tomar:
```

---

## Bloque 5: Plan De Acción Y Pitch Ejecutivo (65 min)

### Objetivo

Transformar análisis en una decisión ejecutiva defendible, con experimento de bajo riesgo y métrica de éxito.

### Dinámica

Cada equipo toma el mini mapa de decisión del bloque anterior y lo convierte en una recomendación ejecutiva. La clave es no brincar de "encontramos un insight" a "hagamos una iniciativa grande"; primero deben diseñar una acción concreta, pequeña y medible.

Antes de escribir el plan, cada equipo debe responder:

- ¿Qué decisión sí podemos tomar con la evidencia actual?
- ¿Qué decisión sería prematura?
- ¿Qué riesgo estamos aceptando si actuamos?
- ¿Qué riesgo estamos aceptando si no actuamos?
- ¿Qué experimento de 30 días nos permitiría aprender sin comprometer demasiado tiempo, presupuesto o reputación?

### Prompt Maestro 4: Plan De Acción

```text
Actúa como un líder senior de estrategia y transformación con IA.

Con base en este análisis:

<analisis>
[Pegar el mini mapa de decisión del bloque anterior: hipótesis más probable, evidencia principal, nivel de confianza, dato que falta y decisiones posibles]
</analisis>

Ayúdame a construir un plan de acción defendible para presentar a liderazgo.

Formato:
1. Decisión recomendada.
2. Evidencia principal.
3. Qué sabemos con confianza.
4. Qué todavía no sabemos.
5. Riesgos de actuar.
6. Riesgos de no actuar.
7. Supuestos que debemos declarar.
8. Primer experimento de bajo riesgo en 30 días.
9. Métrica de éxito.
10. Señales tempranas que revisaríamos en 2 semanas.
11. Mensaje ejecutivo en máximo 150 palabras.

Reglas:
- No propongas iniciativas genéricas.
- Conecta cada acción con evidencia.
- Declara límites y supuestos.
- Prioriza acciones que puedan probarse rápido.
- Si la evidencia no alcanza para recomendar acción, propón un experimento de aprendizaje, no una decisión definitiva.
```

### Actividad: De Insight A Acción

Cada equipo convierte el output de la IA en un plan propio. No deben copiar la respuesta tal cual; deben editarla con criterio de negocio.

Checklist del plan:

- La decisión recomendada es específica.
- La acción puede iniciarse en 30 días.
- La métrica mide impacto, no solo actividad.
- Los supuestos están declarados.
- El plan reconoce qué dato falta.
- La recomendación no promete más de lo que la evidencia permite.

### Pitch Ejecutivo

Cada equipo presenta en 4 minutos:

1. Problema definido.
2. Pregunta estratégica.
3. Hipótesis investigada.
4. Evidencia más importante.
5. Decisión recomendada.
6. Riesgo principal de actuar o no actuar.
7. Experimento de 30 días.
8. Métrica de éxito.

### Criterios De Evaluación

El grupo evalúa cada pitch con estas preguntas:

- ¿El problema está claramente definido?
- ¿La recomendación se desprende de la evidencia?
- ¿El equipo declaró límites y riesgos?
- ¿El experimento es realista en 30 días?
- ¿La métrica de éxito mide impacto, no solo actividad?

---

## Plantilla Final: AI Decision Brief

```markdown
# AI Decision Brief

## 1. Contexto
[Qué proceso, tribu o decisión estamos analizando]

## 2. Problema Definido
Queremos entender si [causa/patrón] está afectando [resultado] en [población/proceso], para decidir [acción].

## 3. Pregunta Estratégica
[Pregunta prioritaria]

## 4. Hipótesis
- Hipótesis principal:
- Hipótesis alternativa:

## 5. Evidencia
- Evidencia que apoya:
- Evidencia que contradice:
- Patrones relevantes:

## 6. Nivel De Confianza
Alto / Medio / Bajo

Por qué:

## 7. Límites Del Análisis
- Qué no podemos afirmar:
- Qué dato falta:
- Qué supuesto estamos haciendo:

## 8. Riesgos Y Supuestos
- Riesgo de actuar:
- Riesgo de no actuar:
- Supuesto principal:

## 9. Decisión Recomendada
[Decisión concreta]

## 10. Experimento De 30 Días
- Acción:
- Dueño:
- Población o alcance:
- Métrica de éxito:
- Señales a revisar en 2 semanas:

## 11. Mensaje Ejecutivo
[Máximo 150 palabras]
```

---

## Cierre Del Workshop (10 min)

### Reflexión Silenciosa (2 min)

Cada participante responde en silencio:

```text
La próxima vez que use IA para una decisión importante, antes de pedirle una respuesta voy a pedirle que me ayude a:
```

### Reflexión Grupal (5 min)

Preguntas para abrir al grupo:

- ¿Qué parte del proceso cambió más tu forma de pensar: preguntar, definir el problema, formular hipótesis, analizar evidencia o diseñar acción?
- ¿Qué caso real de tu tribu podrías trabajar con este método en los próximos 30 días?

### Cierre Grupal (3 min)

Pregunta final al grupo:

> ¿Qué tendría que pasar para que usar IA en decisiones importantes se vuelva una práctica de equipo, no solo una habilidad individual?
