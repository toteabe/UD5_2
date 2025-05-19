### 1. Definición y propósito

Un diagrama de secuencia muestra cómo un conjunto de participantes colabora para ejecutar un único escenario o caso de uso, capturando de forma ordenada los mensajes intercambiados y el paso del tiempo de arriba hacia abajo. Es la forma más común de diagrama de interacción en UML, ideal para visualizar la colaboración y el flujo de llamadas entre objetos “tal cual” ocurre en un escenario concreto .

---

### 2. Participantes y notación básica

- **Líneas de vida (lifelines):** cada participante—ya sea un objeto, rol o componente—se representa con una línea vertical que marca su existencia durante la interacción.
    
- **Barras de activación:** un rectángulo estrecho sobre la línea de vida indica cuándo ese participante está “activo” (es decir, ejecutando uno de sus métodos) .
    
- **Mensajes:** flechas entre líneas de vida que representan invocaciones:
    
    - **Sincrónicas:** flecha con punta rellena (el llamador espera respuesta).
        
    - **Asíncronas:** flecha con barra (el llamador continúa sin bloquearse) .
        
- **Retornos y parámetros:** el paso de datos se muestra como parte del nombre del mensaje o con flechas de retorno opcionales; se usan solo cuando añaden claridad .
    
- **Mensaje “encontrado”:** flecha inicial sin origen definido, para eventos que llegan del exterior.
    

---

### 3. Estilos de control: centralizado vs. distribuido

- **Control centralizado:** un único participante orquesta casi todo el procesamiento, solicitando datos o servicios a los demás (Figura 4.1). Es más sencillo de leer al concentrar la lógica en un solo punto .
![[Figura4.1.png]]

    
- **Control distribuido:** cada participante asume pequeñas responsabilidades y colabora delegando entre sí (Figura 4.2). Favorece la cohesión de datos y comportamiento, facilita el uso de polimorfismo y reduce los efectos colaterales de los cambios .
![[Figura4.2.png]]

---

### 4. Creación y eliminación de participantes

- **Creación:** se dibuja la flecha al cuadro del nuevo participante (a menudo etiquetada `new`); si actúa inmediatamente, comienza su activación tras el cuadro .

- **Eliminación:** una gran “X” al final de la línea de vida o en la punta de la flecha que lo borra; útil incluso en entornos con recolección de basura para indicar cierre de recursos .
![[Figura4.3.png]]   

---

### 5. Lógica de control: marcos de interacción

Para representar bucles, condicionales y paralelismo UML 2 introduce **fragmentos combinados** (frames):

|Operador|Significado|
|---|---|
|`loop`|Bucle con guarda que indica la base de iteración|
|`alt`|Alternativa entre fragmentos mutuamente excluyentes|
|`opt`|Opcional (equivalente a `alt` con un solo fragmento)|
|`par`|Paralelismo|
|`region`|Región crítica (un solo hilo a la vez)|
|`neg`|Interacción inválida|
|`ref`|Referencia a otro diagrama de interacción|

Cada fragmento lleva una condición (guarda) que controla su ejecución; sin embargo, muchos diseñadores prefieren pseudomensajes o notaciones antiguas por ser más ligeras .

![[Figura4.4.png]]

---

### 6. Mensajes síncronos vs. asíncronos

En UML 2 la punta de flecha rellena indica síncrono (bloqueante) y la de barra asíncrono (no bloqueante). La asíncronía mejora la capacidad de respuesta y reduce el acoplamiento temporal, pero complica la depuración. Dado lo sutil del cambio en la punta, a veces se sigue usando la flecha de “medio palo” de UML 1 para destacar mejor la asincronía.

![[Figura4.5.png]]

---

### 7. Cuándo utilizar diagramas de secuencia

Úsalos cuando necesites:

- **Visualizar la colaboración** entre varios objetos en un mismo caso de uso.
    
- **Documentar flujo de mensajes** en escenarios concretos (por ejemplo, login, checkout).  
    No son ideales para detallar algoritmos complejos ni múltiples [[Casos de uso]] para eso convienen diagramas de estados o de actividad .
    

---

### 8. Tarjetas CRC como complemento

Las **tarjetas CRC** (Clase–Responsabilidad–Colaboración) son una técnica ligera previa al diagrama, donde en cada tarjeta se anota:

- **Clase**
    
- **Responsabilidades** (operaciones, decisiones, datos clave)
    
- **Colaboradores** (otras clases implicadas)
    

Se usan en sesiones de diseño para explorar rápidamente alternativas moviendo y “jugando” con las tarjetas, antes de plasmar el diagrama formal. Fomentan debate y ayudan a refinar responsabilidades de alto nivel sin caer en listas demasiado detalladas .

![[Figura4.6.png]]

---
