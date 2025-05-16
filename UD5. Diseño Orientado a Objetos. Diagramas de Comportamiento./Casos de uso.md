### 1. ¿Qué es un caso de uso?

Un **caso de uso** agrupa varios **escenarios** que comparten un mismo objetivo de usuario. Cada escenario es una secuencia concreta de pasos en la que el actor interactúa con el sistema. Aunque los escenarios puedan fallar o variar, el objetivo común (“comprar un producto”, “registrarse”, etc.) permanece constante .

---

## 2. Actores

- Un **actor** es el rol que desempeña un usuario o sistema externo frente a nuestro sistema.
    
- **Actor principal**: quien inicia el caso de uso y tiene el objetivo tratado.
    
- **Actores secundarios**: colaboran durante la ejecución (por ejemplo, un servicio de pagos) .
    

---

## 3. Estructura textual de un caso de uso

1. **Escenario principal de éxito**
    
    - Lista numerada de pasos que describen la interacción ideal, enfatizando la intención del actor (“El cliente explora el catálogo…”), sin mencionar detalles de interfaz ni diseño interno. Ver figura 9.1
![[Figura9.1.png]]
1. **Extensiones** (flujos alternativos y de excepción)
    
    - Se nombran según el paso donde ocurren (p. ej. “3a”, “6a”), describen la condición y los pasos concretos, y luego indican dónde regresan al flujo principal o terminan.
        
2. **Inclusiones**
    
    - Un paso complejo puede referenciar otro caso de uso (incluir), escrito habitualmente subrayado para sugerir un “hipervínculo” a un texto o documento aparte.
        
3. **Elementos opcionales**
    
    - **Precondiciones:** lo que debe ser verdadero antes de iniciar.
        
    - **Postcondiciones o garantías:** lo que el sistema asegura tras un éxito o, como mínimo, en cualquier caso.
        
    - **Desencadenante (trigger):** evento que inicia el caso de uso (p. ej. “Usuario pulsa ‘Pagar’”) .
        

---

## 4. Generación de extensiones

Para cada paso del flujo principal, pregúntate “¿qué podría salir mal?” o “¿cómo podría variar esto?”. Es recomendable listar **todas** las condiciones de extensión antes de profundizar en sus detalles, así reduces el riesgo de omitir casos de fallo o variación importantes .

---

## 5. Diagramas de casos de uso

- UML sólo estandariza la **notación gráfica** (óvalos para casos de uso, palitos para actores, relaciones «include»/«extend»).
![[Figura9.2.png]]

- Sirven principalmente como “tabla de contenido” para los casos de uso textuales, mostrando límites del sistema y qué actores ejecutan cada caso.
    
- **Extiende** («extend») rara vez aporta valor y suele generar confusión; es preferible describir extensiones en texto .

  

---

## 6. Niveles de casos de uso (Cockburn)

- **Nivel del mar (sea-level)**: casos discretos, valor directo al actor, duración de minutos a media hora (la mayoría de los casos de uso de sistema).
    
- **Nivel de peces (fish-level)**: subfunciones internas del sistema, documentadas sólo si se reutilizan.
    
- **Nivel de cometa (kite-level)**: procesos empresariales de alto nivel, integran varios casos de uso de “nivel del mar”.
    
- Se recomienda indicar el nivel en la cabecera de cada caso para contextualizar su alcance .
    

---

## 7. Casos de uso vs. características (historias)

- Las **historias de usuario** fragmentan el trabajo para iteraciones ágiles.
    
- Puedes derivar historias de un caso de uso completo, de un escenario o incluso de cada extensión.
    
- Las características suelen ser más detalladas, pero parten de la visión global que aportan los casos de uso .
    

---

## 8. Cuándo y cómo usarlos

- **Uso temprano:** revisar todos los casos de uso para validar requisitos funcionales.
    
- **Detalle justo a tiempo:** documentar versiones más completas de los casos críticos justo antes de implementarlos.
    
- Mantén los casos **breves** (1–2 páginas). Un documento muy largo apenas se lee; uno muy corto siempre puede ampliarse según se avance .
    

---

## 9. Buenas prácticas de redacción

- Emplea **lenguaje de intención**: qué quiere el actor, no cómo se muestra la UI ni cómo se programa internamente.
    
- Sé **específico** en los pasos, pero evita detalles superfluos.
    
- Usa **sesiones CRC** (Clase–Responsabilidad–Colaboración, ver [[Diagramas de secuencia#8. Tarjetas CRC como complemento]]) para explorar interacciones antes de formalizar el texto.
    
- Revisa periódicamente y actualiza los casos según evolucione el sistema .
    

---