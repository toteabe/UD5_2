Los diagramas de interacción en UML son un subconjunto de los diagramas de comportamiento orientados a modelar cómo los objetos colaboran entre sí para llevar a cabo una funcionalidad o un caso de uso concreto, prestando especial atención al flujo de mensajes y al orden en que estos se intercambian.

## ¿Para qué sirven?

- **Visualizar el flujo de control y datos** entre instancias (objetos, componentes) a lo largo del tiempo.

- **Aclarar requisitos** de interacción antes de la implementación, detectando posibles errores de diseño.
   
- **Documentar** de forma estandarizada cómo los distintos elementos de un sistema colaboran para cumplir un servicio.
   
## Elementos básicos comunes

1. **Líneas de vida (lifelines):** representan las instancias u objetos participantes.
   
2. **Mensajes:** flechas que indican llamadas a métodos, devoluciones o señales.
   
3. **Activación (focus of control):** rectángulo estrecho sobre la línea de vida que señala cuándo el objeto está ocupado procesando.
   
4. **Guardas y fragmentos combinados:** para modelar fragmentos condicionales (`alt`), iterativos (`loop`), paralelos (`par`), entre otros.
   

---

## Tipos principales de diagramas de interacción

### 1. [[Diagramas de secuencia]](Sequence Diagrams)

- **Qué muestra:** el orden cronológico de los mensajes entre participantes.
   
- **Cuándo usarlo:** para detallar el flujo exacto de llamadas en un escenario concreto, p. ej. la creación de una orden de compra.
   
- **Características clave:**
   
   - Eje vertical: paso del tiempo (de arriba abajo).
   
   - Eje horizontal: diferentes objetos.
   
   - Muy útil para detectar dependencias temporales y posibles bloqueos.
   

### 2. Diagrama de Comunicación (Communication Diagram)

- **Qué muestra:** las mismas interacciones que el de secuencia, pero enfatizando las relaciones (links) entre objetos y numerando los mensajes para indicar el orden.
   
- **Cuándo usarlo:** cuando la topología de conexiones importa más que la línea temporal exacta.
   
- **Características clave:**
   
   - Los objetos se colocan libremente; los enlaces muestran quién se comunica con quién.
   
   - Cada mensaje va numerado (1, 1.1, 1.2, 2…) para reflejar la secuencia.
   

### 3. Diagrama de Visión General de Interacción (Interaction Overview Diagram)

- **Qué muestra:** un “mapa” de sub-flujos de interacción, combinando fragmentos de secuencia y de actividad.
   
- **Cuándo usarlo:** para modelar procesos complejos compuestos de múltiples escenarios de interacción.
   
- **Características clave:**
   
   - Usa nodos de “fragmento combinado” (`interactionOccurrence`) que referencian otros diagramas de interacción.
   
  - Permite estructurar de forma modular grandes procesos.
   

### 4. Diagrama de Temporización (Timing Diagram)

- **Qué muestra:** el cambio de estado o valor de un objeto/parte a lo largo de una escala temporal precisa.
   
- **Cuándo usarlo:** en sistemas muy sensibles al tiempo (embebidos, telecomunicaciones), para verificar restricciones temporales.
   
- **Características clave:**
   
   - Cada línea de vida incluye una gráfica de estado/valor en función del tiempo.
   
   - Ideal para modelar retardos, ventanas de tiempo y sincronización.
   

---

## Beneficios de usar diagramas de interacción

- **Detección temprana de errores** en la lógica de colaboración.
   
- **Comunicación clara** entre analistas, diseñadores y desarrolladores.
   
- **Documentación viva** que puede actualizarse conforme evoluciona el sistema.
   
- **Soporte de herramientas**: la mayoría de suites UML (Enterprise Architect, MagicDraw, Visual Paradigm…) generan incluso esqueletos de código a partir de estos diagramas.
   

