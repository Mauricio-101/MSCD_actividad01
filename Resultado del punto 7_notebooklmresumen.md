# Ingeniería del Conocimiento y Sistemas Expertos Basados en Reglas

## Documento Informativo

Este documento sintetiza los principios, metodologías y estructuras fundamentales de la Ingeniería del Conocimiento (IC) y los Sistemas Expertos (SE), basándose en el análisis exhaustivo del material proporcionado.

# 1. Fundamentos de la Ingeniería del Conocimiento (IC)

La Ingeniería del Conocimiento es una disciplina vinculada a la Inteligencia Artificial que se ocupa de la adquisición, representación, validación, inferenciación, explicación y mantenimiento del conocimiento. Su objetivo primordial es construir sistemas que emulen el comportamiento inteligente de un experto humano en dominios específicos.

## Conceptos Clave

- **Conocimiento:** Desde la IA, es la combinación de esquemas de datos y procedimientos interpretativos que permiten un comportamiento inteligente. Está formado por hechos, conceptos, reglas y asociaciones.

- **Ingeniero del Conocimiento (ICO):** Especialista informático que extrae el conocimiento de los expertos, conoce herramientas de desarrollo y posee habilidades de comunicación y psicología para interpretar al experto.

- **Experto Humano:** Persona de prestigio que pone su experiencia a disposición del sistema.

- **Usuario:** Persona que utilizará el sistema y cuyas necesidades deben considerarse en el desarrollo.

## Tipos de Conocimiento

| Tipo | Descripción |
|------|-------------|
| Declarativo | Expresa hechos, atributos de objetos o conceptos y sus relaciones. |
| Procedural | Conjunto de reglas que los expertos usan para solucionar problemas y generar nuevo conocimiento. |
| Metaconocimiento | Conocimiento sobre el propio conocimiento y las capacidades de razonamiento del sistema. |

---

# 2. El Proceso de Adquisición del Conocimiento (AC)

La adquisición es el proceso central de extracción de conocimiento de diversas fuentes para su automatización.

## Fuentes de Conocimiento

1. **Estáticas (Secundarias):** Contenido que no varía, como libros, revistas o artículos.
2. **Dinámicas (Primarias):** Basadas en la experiencia, son variables y cambiantes; el experto humano es la fuente principal.

## Etapas de la Adquisición (Modelo de Vázquez, 2009)

1. **Identificación:** Reconocimiento del problema, división en subproblemas e identificación de participantes y recursos.
2. **Entendimiento:** Determinación de conceptos y relaciones, y definición de la forma de representación.
3. **Formalización:** Organización del conocimiento en la Base de Conocimiento (BC), mezclándose con la fase de representación.
4. **Implementación:** Programación del conocimiento en la computadora y desarrollo de un prototipo.
5. **Pruebas:** Validación del conocimiento mediante ejemplos y revisión por parte del experto.

---

# 3. Representación del Conocimiento (KR)

La KR consiste en llevar el conocimiento extraído a una forma inteligible y organizada. Una buena representación debe ser sencilla, fácil de modificar, transparente, independiente y relacional.

## Esquemas de Representación

- **Reglas de Lógica Simbólica:** Utiliza lógica proposicional (booleana) y lógica de predicados (sintaxis formal con constantes, variables, funciones y cuantificadores).

- **Redes Semánticas (Redes Asociativas):** Representación gráfica de relaciones entre nodos (objetos/atributos) y enlaces (arcos). Las relaciones más comunes son **"ES-UN"** y **"ES-SUBCONJUNTO"**.

- **Frames (Marcos) o Slots:** Estructuras de datos para representar objetos y situaciones divididos en componentes (slots) y facetas (atributos). Permiten herencia jerárquica.

- **Árboles de Decisión:** Representan espacios de búsqueda donde los nodos son metas y las ramas son decisiones o resultados.

- **Gráficos Conceptuales:** Expresan relaciones secuenciales, jerárquicas y de causa-efecto para resolver problemas.

- **Diagramas Lógicos:** Clasificados en esquemas declarativos (hechos estáticos) y procedimentales (reglas dinámicas).

---

# 4. Sistemas Expertos Basados en Reglas

Estos sistemas son herramientas eficientes para situaciones complejas regidas por reglas deterministas (ej. transacciones bancarias, sistemas de seguridad).

## Componentes del Sistema

- **Base de Conocimiento:** Contiene los **Hechos** (conocimiento dinámico, temporal y específico de una aplicación) y las **Reglas** (conocimiento estático, permanente y general).

- **Motor de Inferencia:** Aplica la lógica a los hechos y reglas para obtener conclusiones.

- **Subsistema de Control de Coherencia:** Asegura que no existan contradicciones.

- **Subsistema de Explicación:** Justifica las conclusiones alcanzadas.

## Definición y Estructura de una Regla

Una regla es una afirmación lógica:

> **Si Premisa, entonces Conclusión**

- **Premisa (Antecedente):** Expresión lógica con una o más afirmaciones objeto-valor conectadas por operadores (y, o, no).

- **Conclusión (Consecuente):** Resultado lógico que se deriva si la premisa es cierta.

### Sustitución de reglas

Para facilitar la programación, reglas complejas pueden reemplazarse por conjuntos de reglas equivalentes.

Por ejemplo:

```
Si A o B, entonces C
```

se sustituye por:

```
Si A, entonces C
Si B, entonces C
```

---

# 5. El Motor de Inferencia: Estrategias de Razonamiento

El motor de inferencia interpreta las reglas mediante el reconocimiento de patrones, la resolución de conflictos y la ejecución.

## Reglas de Inferencia Básicas

1. **Modus Ponens:** Si "A implica B" y "A es cierto", entonces "B es cierto". Se mueve hacia adelante, de la premisa a la conclusión.

2. **Modus Tollens:** Si "A implica B" y "B es falso", entonces "A es falso". Se mueve hacia atrás, de la conclusión a la premisa.

3. **Mecanismo de Resolución:** Utilizado para conclusiones compuestas. Combina expresiones lógicas equivalentes para simplificar y obtener resultados.

## Estrategias de Encadenamiento

- **Encadenamiento de Reglas (Hacia adelante):** Parte de los hechos conocidos para derivar nuevos hechos hasta que no se puedan obtener más conclusiones.

- **Encadenamiento Orientado a Objetivo (Hacia atrás):** El usuario selecciona una variable objetivo y el sistema navega por las reglas buscando una conclusión. Si falta información, el sistema pregunta al usuario.

- **Compilación de Reglas:** Escribe los objetivos en función de los datos iniciales mediante "ecuaciones objetivo" para obtener resultados inmediatos.

---

# 6. Coherencia y Validación del Conocimiento

La integridad de un sistema experto depende de la consistencia de su información.

- **Coherencia de Reglas:** Un conjunto es coherente si existe al menos un conjunto de valores que no produzca conclusiones contradictorias.

- **Valores No Factibles:** Valores que, de ser asignados a un objeto, contradicen cualquier combinación de valores del resto de objetos. Estos deben ser eliminados de las listas de opciones del usuario.

- **Validación:** Proceso de asegurar que el trabajo del sistema sea igual al que realizaría un experto humano en la realidad.

- **Hipótesis del Mundo Cerrado:** Si algo no puede demostrarse como cierto, se asume que es falso.

---

# 7. Métodos de Adquisición del Conocimiento

| Categoría | Métodos y Técnicas |
|-----------|--------------------|
| Manuales | Entrevistas (estructuradas, semiestructuradas, no estructuradas), Análisis de protocolo (observación de la trayectoria del pensamiento), Lluvia de ideas, Casos de análisis, Prototipos. |
| Semiautomatizados | Herramientas de soporte al Experto (Análisis de Rejilla/Teoría de Kelly) y soporte al ICO (Editores, interfaces, herramientas de documentación). |
| Automatizados | Reglas de Inducción Automatizadas (algoritmo ID3 para convertir matrices en árboles de decisión) y Aprendizaje Automatizado (heurísticas para aprender de la experiencia). |